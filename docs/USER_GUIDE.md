# Echo Desktop — User Guide (1.10.0)

## First launch
Install using the Windows setup package described in `WINDOWS_BUILD_AND_INSTALL.md`. Local playback does not require an online streaming account. Internet is needed for optional lookups and some one-time setup tasks.

## Import music
- **Import music** selects one or more audio files.
- **Import folder** adds a folder of music.
- Wait for the import summary.
- Edit a track to correct metadata, add artwork or add lyrics.

Formats mentioned in project troubleshooting notes include MP3, M4A/AAC, WAV, OGG/Opus and FLAC. Actual codec support depends on the runtime/media stack.

## Search
Use the top search field or **Ctrl + L**. Search covers the local library, including documented fields such as title, artist, album, album artist, genre and filename. It is not online streaming search.

## Playlists and queue
Create playlists from the library controls and add tracks using the playlist action. Open Queue from the bottom player. Drag the dotted handle to reorder; dragging should not restart the current track. Shuffle prepares a fixed order for the session; Next and Previous follow that order.

## Metadata and artwork
1. Open **Edit** on a track.
2. Choose **Fetch metadata online**.
3. Review candidate title, artist, album, release information and artwork.
4. Select the correct recording/release and save.
5. If no suitable result appears, edit manually.

## Lyrics
You can import LRC/TXT, paste text or enter lyrics manually. To fetch lyrics, open Edit and choose **Fetch lyrics online**. Check title, artist, album, duration, provider and timing quality before applying. Public services may be incomplete or rate-limited.

### Full-screen lyrics
Open using the expand icon beside LYRICS or the LYR button in the bottom player. Scroll vertically; manual scrolling pauses Follow active. Select **Follow active** to resume auto-follow. Click a timestamped line to seek. Use **Hide timeline / Show timeline** to control the synchronized playback timeline. The scrollbar is visually hidden while scrolling remains available.

### Timing correction
- **Timing offset:** corrects a constant early/late shift. Negative moves earlier; positive moves later.
- **Timing drift / speed:** corrects gradual timing drift. 100% is the original scale.
- **Reset timing:** returns to 0 ms and 100%.

A global offset/rate cannot repair unrelated individual timestamp errors. Edit those lines or choose a better synced version.

## Optional local lyric alignment
This aligns lyric text already supplied by the user; it is not a missing-lyrics generator.
1. In Edit Track > Lyrics, paste or fetch lyrics.
2. Choose Auto detect, English, Hindi, Urdu or Punjabi.
3. Choose Fast · Tiny or Balanced · Base.
4. Select **Align timestamps** and wait for model loading, audio scanning, matching and preview.
5. Review matched and unmatched lines; correct errors before saving.

The Start Menu helper **Install Echo Lyric Aligner** sets up the optional private `.echo-lyric-venv` environment. It installs/verifies faster-whisper and lyric-align and writes `Echo-Lyric-Aligner-Setup.log`. The first alignment run downloads the selected model. Normal playback, library, playlists and manual/provider lyrics do not require Python.

## Artwork and visualizer
Click the Now Playing artwork tile or expand control. The full-screen view includes Visualizer On/Off. Live visualization depends on audio analysis being available.

## Keyboard shortcuts

| Shortcut | Action |
|---|---|
| Space | Play / pause |
| Left / Right | Seek 5 seconds backward / forward |
| Ctrl + O | Import songs |
| Ctrl + L | Focus library search |
| Ctrl + Q | Open queue |
| Esc | Close dialog or full-screen view |

Space on a focused button should still activate that button normally.

## Data safety
Database: `echo-desktop-library`; schema version: `2`; stable origin: `http://127.0.0.1:43127`. Do not clear Echo app/site data. Keep original audio files backed up separately. Confirm the library is present after updates before deleting backups.
