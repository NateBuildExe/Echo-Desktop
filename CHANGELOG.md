# Changelog

Historical entries are based on release/installation notes available when this documentation was prepared. Older patch-level history is incomplete.

## [1.10.0] — 2026-11-15

### Added
- Optional local lyric timestamp alignment for lyrics already supplied by the user.
- Language choices: Auto detect, English, Hindi, Urdu and Punjabi.
- Fast · Tiny and Balanced · Base model choices.
- Live progress percentage and phase messages for alignment.
- Branded NSIS Windows installer and Windows build helper.
- Start Menu helper for optional lyric-align setup.

### Improved
- Alignment uses the same private Python environment verified by setup.
- Setup verifies faster-whisper and lyric-align and writes `Echo-Lyric-Aligner-Setup.log`.
- Full-screen lyrics remain scrollable while the visible scrollbar is hidden/clipped.
- Alignment preview reports matched lines and leaves unmatched text for review.

### Notes
- Alignment is optional; normal playback and manual/provider lyrics do not require Python.
- Alignment timestamps supplied lyrics; it does not generate missing copyrighted lyrics.
- SoundCloud keyword search is not active without official API credentials.
- Installer is unsigned.
- Owner-reported Windows installer acceptance passed on 15 November 2026. See `docs/TEST_LOG.md`.

## [1.9.3] — documented improvements
- Full-screen artwork from Now Playing, with Visualizer On/Off.
- Visualizer follows live audio when analysis is available and shows ambient preview while paused/unavailable.
- Import progress and final summary.
- Timeout for problematic audio-duration probing.
- Keyboard shortcuts documented in Settings.
- Library sort preference persists.
- Like disabled until a track is loaded.

## [1.9.x] — cumulative documented features; exact patch introduction not confirmed
- Multi-term local search.
- Fixed shuffle queue order and Next/Previous navigation.
- Scrollable full-screen lyrics with Follow active and synchronized timeline.
- Lyric timing offset and drift/speed correction.
- Safer row interactions.
- Expanded metadata search using MusicBrainz and Apple/iTunes.
- Multiple lyric providers with provider/timing quality display.

## [1.9.0] — documented baseline
- Windows installation/update guide.
- Music metadata and artwork lookup.
- Lyrics lookup, manual editing and LRC/TXT import.
- Full-screen lyrics and artwork.
- Queue reordering.
- Local library and playback data retention through documented updates.

## [1.8.1] — documented notes
- MusicBrainz metadata lookup, Cover Art Archive artwork and LRCLIB lyrics.
- Manual metadata editing and lyric import.
- Existing library, playlists, artwork and lyrics documented as preserved across updates.

## [1.8.0] — documented notes
- Local music library, playback, playlists, favourites, queue, shuffle, repeat, artwork and lyrics.
- Metadata and lyric lookup tools.
- Stable local database identity and origin across documented updates.

## Earlier versions
Available 1.7-era notes describe a YouTube Music-category search/embedded-player experiment. This is historical context, not a guaranteed 1.10.0 feature.
