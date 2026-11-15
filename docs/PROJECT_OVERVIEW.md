# Echo Desktop — Project Overview

**Document version:** 1.0 | **Application:** 1.10.0 | **Updated:** 15 November 2026

## Purpose

Echo Desktop is an offline-first Windows music player for importing, organizing and playing a personal local audio library. Optional online tools help locate metadata, artwork and lyrics.

## Product principles

1. Local-first playback.
2. User-controlled imports, playlists and favourites.
3. Review online metadata and lyric candidates before saving.
4. Preserve the existing local library across updates.
5. Keep advanced lyric alignment optional.

## Main feature areas

### Library and playback
- Import one or more audio files or a folder.
- Search the local library; this is not an online streaming search.
- Play tracks, create playlists, like tracks, manage queue, shuffle and repeat.
- Reorder the queue using its dotted drag handle.

### Metadata and artwork
- Documented catalogue sources: MusicBrainz and Apple/iTunes.
- Review candidate title, artist, album, release information and artwork before saving.
- SoundCloud keyword search is not active in the documented 1.10.0 build because the official search API requires registered credentials; public oEmbed is not keyword search.

### Lyrics
- Import LRC/TXT, paste or edit lyrics manually.
- Documented providers include YouLy+ / LyricsPlus, KuGou through Better Lyrics API, and LRCLIB fallback.
- Full-screen lyrics scroll; manual scrolling pauses Follow active until resumed.
- Timestamped lines can seek playback.
- Offset and drift/speed controls correct global timing differences. They cannot repair arbitrary individual line errors.

### Local lyric alignment
Version 1.10.0 can align timestamps for lyric text the user already has. It does not generate missing copyrighted lyrics from audio. Language options documented: Auto detect, English, Hindi, Urdu and Punjabi. Model options: Fast · Tiny and Balanced · Base. Matched lines receive proposed timestamps; unmatched lines remain for review. Users should inspect results before saving. The first model download may be substantial and alignment may be slow on older CPUs.

### Artwork and visualizer
The Now Playing artwork can open full-screen. The view includes a Visualizer On/Off control. Live visualization depends on audio analysis being available.

## Technical baseline

| Area | Documented value |
|---|---|
| Desktop runtime | Electron 45.3.2 |
| Local database | IndexedDB |
| Database name | `echo-desktop-library` |
| Schema version | 2 |
| Stable origin | `http://127.0.0.1:43127` |
| Windows target | Windows 10/11, 64-bit |
| Installer | NSIS, per-user |
| Output | `Echo-Desktop-Setup-1.10.0-x64.exe` |

The GitHub repository receiving this documentation did not contain the application source tree when the docs were prepared. Exact frontend framework, module layout and implementation details are therefore intentionally not guessed.

## Data and privacy

The local library is stored in the Electron/Chromium profile using IndexedDB. The installer is designed to separate program files from the user profile. Uninstall should remove the program while retaining the profile/library. Back up original audio files and important data separately. Do not clear app/site data as a troubleshooting shortcut.

Ordinary local playback is designed to work offline. Online lookups send search information needed by the relevant service. Local lyric alignment processes the audio and supplied lyric text on-device; the documented integration does not upload the audio file.

## Limitations

- Public metadata and lyric catalogues may be incomplete or rate-limited.
- Alignment accuracy varies with vocals, mix, language and lyric formatting.
- The installer is unsigned.
- UI screenshots and application source are pending in this repository.
