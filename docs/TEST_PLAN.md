# Echo Desktop — Test Plan

Applies to 1.10.0 and future Windows releases. For every run, record app version, installer filename, Windows edition/build, architecture, tester, date, fresh/upgrade install status, outcome and evidence. Use PASS, FAIL, BLOCKED or NOT TESTED. Never mark a check passed unless it was performed.

## Installer acceptance

| ID | Check | Expected result |
|---|---|---|
| INS-01 | Build on Windows x64 | Build helper produces expected Setup.exe |
| INS-02 | Run Setup.exe | Wizard opens |
| INS-03 | Complete installation | Program installs |
| INS-04 | Launch after install | Echo opens |
| INS-05 | Start Menu shortcut | Exists and launches Echo |
| INS-06 | Desktop shortcut | Exists when selected and launches Echo |
| INS-07 | Existing library after install | Existing songs and saved information remain |
| INS-08 | Uninstall entry | Echo appears in Windows Apps |
| INS-09 | Uninstall | Program files are removed |
| INS-10 | Library after uninstall | Echo profile/library remains intact |

## Library and playback regression

- Import one file, multiple files and a folder.
- Confirm import progress and final summary.
- Search by title, artist and filename.
- Test play, pause, seek and volume.
- Close/reopen and confirm library/preferences persist.
- Test playlist creation and playback.
- Reorder queue with dotted handle.
- Confirm shuffle order remains fixed and Next/Previous follow queue.

## Metadata, lyrics and artwork regression

- Fetch metadata; review and save a correct candidate.
- Import LRC/TXT and fetch lyric candidates.
- Open full-screen lyrics; confirm scrolling and hidden scrollbar.
- Confirm manual scroll pauses Follow active and it resumes on request.
- Click timestamped line to seek.
- Toggle synchronized timeline.
- Test timing offset, drift and reset.
- Test optional alignment progress and review matched/unmatched lines before save.
- Open full-screen artwork and test visualizer toggle.

## Keyboard shortcuts

Space play/pause; Left/Right seek five seconds; Ctrl+O import; Ctrl+L search; Ctrl+Q queue; Esc close. Space on a focused button should activate that button normally.

## Data preservation
- Verify database identity remains `echo-desktop-library`.
- Confirm schema and stable origin are not changed unexpectedly.
- Test upgrade with an existing library.
- Test uninstall and confirm profile/library remains.
- Keep original audio files backed up; do not clear app/site data.

Automated smoke tests and mocked services do not prove live provider availability, every codec, playback on every device, all Windows installer configurations, or lyric-alignment accuracy.
