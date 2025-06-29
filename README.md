# Saika Suite - The Offline-First Digital Hub

## Overview

Saika Suite is a comprehensive, cross-platform software solution built entirely in Python, designed to empower users in environments with limited internet access and high data costs, specifically targeting the Cuban context. It prioritizes offline functionality, extreme data efficiency, and a user-friendly experience, transforming devices into self-sufficient digital hubs for entertainment and productivity.

Saika Suite is the foundational step towards **SaikaOS**, a future Linux-based operating system where Saika Suite will serve as the primary user environment. Developed by **SaikaNET Studio** (founded in 2025 by Dragoland, Kiralizt, Fractor, and OX from the University of Informatics Sciences (UCI) in Cuba), this project merges digital art, software development, and game creation with a unique "Cuban touch."

## Key Features & Modules

Saika Suite is developed in phases, starting with a Minimum Viable Product (MVP) and expanding thereafter.

### MVP Modules (Currently in Focus)

  * **SaikaPlay (Multimedia Player)**: Your "FirePlayer" project forms the core of this module. It's a robust multimedia player designed for local content playback.

      * **Features:** Plays video (MP4, MKV, AVI) and audio files, basic playlist management, essential playback controls (play, pause, stop, skip), volume control, adjustable playback speed, and external subtitle loading (SRT, ASS).
      * **Technologies:** Python, PyQt6, `python-vlc`.

  * **SaikaGrab (Hyper-Optimized Downloader)**: Your "FireDownload" project is integrated here as the primary download manager. It's built for efficient content acquisition with limited connectivity.

      * **Features:** Downloads videos/audios from various platforms (YouTube, TikTok, Instagram, Facebook, etc.) using `yt-dlp`, supports quality and format selection (up to 4K video, various audio formats), robust download resume capabilities, detailed error handling, scheduled downloads, and multi-language support.
      * **Technologies:** Python, PyQt5, `yt-dlp`, `requests`, `subprocess`, `concurrent.futures`.

  * **SaikaVault (Advanced File Manager & Digital Library)**: This module focuses on local file organization and content management.

      * **Features:** File/folder Browse and management (copy, move, delete), thumbnail previews, offline metadata management, and manual tagging for content organization.

### Strategic Expansion Modules (Future Phases)

  * **SaikaWeb (Lightweight & Efficient Web Browser)**: Basic Browse, ad/tracker blocking, "Text-Only" mode, aggressive caching for offline reading, and full webpage saving.
      * **Technologies (Planned):** Python, `requests`, `BeautifulSoup`.
  * **SaikaDoc (Document Reader & Editor)**: View and edit TXT, PDF, ePub, with basic support for DOCX/ODT. Includes offline search, annotation, and text-to-speech.
  * **SaikaShare (P2P Communication & File Sharing)**: File transfer via Wi-Fi Direct/Bluetooth, lightweight FTP/HTTP server for local network sharing, P2P folder synchronization, and offline local chat.
  * **SaikaTools (Expanded Essential Utilities)**: System performance monitor, image/video compressor, cache cleaner, QR code reader/generator, calculator, simplified contact manager, image viewer, offline currency converter (CUP, MLC), offline radio, and weather info.
      * **QR Generator:** Your "app.py" project will be refactored and integrated here as a core utility.
      * **Technologies (Planned/Used):** Python, `psutil`, `qrcode`, `pyzbar`, `opencv-python`.

## Technical Stack

Saika Suite is developed entirely in Python, leveraging its versatility and rich ecosystem of libraries.

  * **Core Language:** Python 3.x
  * **GUI Frameworks:** PyQt6 (for SaikaPlay), PyQt5 (for SaikaGrab), potentially Kivy/KivyMD for Android future.
  * **Multimedia Playback:** `python-vlc`
  * **Content Downloading:** `yt-dlp`
  * **Web Scraping/Parsing:** `requests`, `BeautifulSoup`
  * **System Utilities:** `psutil`, `qrcode`, `pyzbar`, `opencv-python`, `os`, `subprocess`, `time`.
  * **Concurrency:** `concurrent.futures.ThreadPoolExecutor`
  * **Database:** SQLite3 (planned for local data storage)
  * **Packaging:**
      * **Windows:** PyInstaller
      * **Android:** Buildozer
      * **Linux:** PyInstaller, custom shell scripts for `.deb`, AppImage, etc.

## Project Structure

The project follows a well-defined modular structure to ensure scalability, maintainability, and ease of collaboration.

```
saika_suite/
├── .github/                       # GitHub configurations (issue templates, CI/CD workflows)
│   ├── ISSUE_TEMPLATE/            # Templates for bug reports, feature requests, offline feedback
│   └── workflows/                 # GitHub Actions workflows for testing and multi-platform releases
├── docs/                          # Project documentation (installation guides, tutorials, FAQ)
│   ├── guia_instalacion_offline.md
│   ├── tutoriales/
│   ├── FAQ_es.md
│   ├── architecture_overview.md
│   └── CONTRIBUTING.md
├── src/                           # Source code of the application
│   ├── core/                      # Cross-cutting functionalities and base utilities
│   │   ├── config_manager.py      # Global configuration management
│   │   ├── data_monitor.py        # Data consumption monitoring
│   │   ├── offline_feedback.py    # Offline feedback mechanism
│   │   ├── utilities/             # General utilities (e.g., qr_generator.py - your 'app.py' refactored)
│   │   ├── database/              # Local database management (connection, schema)
│   │   └── exceptions.py          # Custom exceptions
│   ├── modules/                   # Main Saika Suite modules
│   │   ├── saikaplay/             # Multimedia Player (based on your 'main.py')
│   │   │   ├── player.py          # VLC playback logic
│   │   │   ├── ui/                # SaikaPlay UI components
│   │   │   ├── playlist_manager.py
│   │   │   └── models.py
│   │   ├── saikagrab/             # Download Manager (based on your 'FireDownload.py')
│   │   │   ├── downloader.py      # yt-dlp integration, core download logic
│   │   │   ├── ui/                # SaikaGrab UI components
│   │   │   ├── resume_logic.py
│   │   │   └── task_scheduler.py
│   │   ├── saikavault/            # File Manager & Digital Library
│   │   │   ├── file_manager.py
│   │   │   ├── metadata_utils.py
│   │   │   ├── ui/
│   │   │   └── search_index.py
│   │   ├── saikaweb/              # Web Browser (future)
│   │   ├── saikadoc/              # Document Reader/Editor (future)
│   │   ├── saikashare/            # P2P Communication/Sharing (future)
│   │   └── saikatools/            # Essential Utilities (QR Scanner, system monitor, etc.)
│   ├── platforms/                 # Platform-specific code
│   │   ├── android/               # Buildozer config, JNI interface for Android
│   │   ├── windows/               # PyInstaller scripts, Windows registry access
│   │   ├── linux/                 # Build scripts for .deb/AppImage, desktop entry generation
│   │   └── cross_platform_utils.py# Cross-platform abstractions
│   ├── resources/                 # Static assets (icons, themes, sounds, QR templates)
│   └── main.py                    # Main entry point for Saika Suite
├── tests/                         # Software tests (unit, integration, performance, functional)
│   ├── unit/
│   ├── integration/
│   ├── performance/
│   ├── functional/
│   └── conftest.py
├── scripts/                       # Utility scripts for development and deployment
│   ├── build_windows.bat
│   ├── build_android.sh
│   ├── build_linux.sh
│   ├── package_paquete.sh         # Script to generate "El Paquete Semanal" distribution
│   ├── setup_dev_env.sh
│   ├── run_tests.sh
│   └── clean.sh
├── .gitignore                     # Git ignore file
├── LICENSE                        # Project license (e.g., GPLv3 + commercial clause)
├── pyproject.toml                 # Project configuration (Poetry/Hatch)
├── requirements.txt               # Primary Python dependencies
├── requirements_android.txt       # Android-specific dependencies
├── requirements_linux.txt         # Linux-specific dependencies
├── README_es.md                   # Project README in Spanish (prioritized)
└── README.md                      # Project README in English
```

## Getting Started

*(This section would typically include detailed instructions. As we haven't covered them yet, I'll put placeholders.)*

1.  **Prerequisites:** Python 3.x, pip, git.
      * For SaikaPlay: VLC media player installed.
      * For SaikaGrab: FFmpeg installed.
2.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/saika-suite.git
    cd saika-suite
    ```
3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    # For Android/Linux specific dependencies:
    # pip install -r requirements_android.txt
    # pip install -r requirements_linux.txt
    ```
4.  **Run the application:**
    ```bash
    python src/main.py
    ```

## Contributing

We welcome contributions\! Please refer to our [CONTRIBUTING.md](https://www.google.com/search?q=docs/CONTRIBUTING.md) for guidelines on how to get involved.

## License

This project is licensed under the [LICENSE](https://www.google.com/search?q=LICENSE) file.

## Contact

For questions or feedback, please open an issue in this repository or contact SaikaNET Studio.

-----
