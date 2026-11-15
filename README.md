# Echo Desktop

**An offline-first Windows music player for a personal local audio library.**

- Documented version: **1.10.0**
- Target: **Windows 10/11, 64-bit**
- Desktop runtime: **Electron 45.3.2**
- Installer: `Echo-Desktop-Setup-1.10.0-x64.exe`

Echo focuses on local music playback and library management. Optional online services provide metadata, artwork and lyric suggestions; ordinary local playback does not depend on an online streaming catalogue.

## Features

- Import individual audio files or entire folders.
- Local playback, playlists, favourites, queue, shuffle, repeat and library search.
- Metadata lookup and artwork through documented catalogue sources.
- Manual lyric editing and LRC/TXT import, plus optional lyric-provider lookup.
- Full-screen synchronized lyrics, manual scrolling, timestamp seeking and timing correction.
- Optional local lyric timestamp alignment for lyrics already supplied by the user.
- Full-screen artwork and audio visualizer.
- Branded per-user Windows installer with Start Menu and desktop shortcuts.

## Documentation

- [Project overview](docs/PROJECT_OVERVIEW.md)
- [User guide](docs/USER_GUIDE.md)
- [Windows build and install](docs/WINDOWS_BUILD_AND_INSTALL.md)
- [Changelog](CHANGELOG.md)
- [Test plan](docs/TEST_PLAN.md)
- [Test log](docs/TEST_LOG.md)
- [UI screenshots](docs/screenshots/README.md)

## Data safety

Documented library storage: IndexedDB database `echo-desktop-library`, schema version `2`, stable local origin `http://127.0.0.1:43127`. Keep independent backups of original audio and important library data. Do not clear Echo's app/site data during updates.

The installer is designed to keep the app profile separate from program files. The project owner reported that the 1.10.0 installation and uninstall checks passed and that the existing library remained intact.

## Repository status

This documentation package does not include the full application source tree or compiled installer. UI screenshots are pending and will be added when supplied. The installer is unsigned; Windows may show an unknown-publisher/SmartScreen warning. Do not disable Windows security to install it.

No software license is specified yet. Do not assume reuse or redistribution rights.
