# Echo Desktop — Windows Build and Install (1.10.0)

## Package and requirements
The documented 1.10.0 build package contains the app source, branded NSIS installer configuration, `Build-Echo-Installer.bat`, and optional lyric-align setup helper.

Requirements:
- 64-bit Windows 10/11.
- Node.js 20+; Node.js 22 LTS recommended.
- Internet for one-time npm packaging-tool installation.
- Keep the existing `node_modules` folder if it already contains Electron 45.3.2.

The GitHub repository currently contains documentation only; the source/build package is required to execute these steps.

## Build
1. Extract the Echo 1.10.0 source/build package to a normal writable folder.
2. If reusing the existing project folder, merge updated source into it and keep `node_modules`. Otherwise install Node.js 22 LTS or newer.
3. Double-click `Build-Echo-Installer.bat`.
4. Keep the terminal open while the helper installs the pinned packaging tool, runs smoke tests and builds the NSIS installer.
5. Output: `dist\Echo-Desktop-Setup-1.10.0-x64.exe`.

The Windows NSIS packaging toolchain must be run on Windows x64.

## Install
1. Run `Echo-Desktop-Setup-1.10.0-x64.exe`.
2. Follow the wizard and choose an install folder if desired.
3. Select Start Menu and desktop shortcuts as required.
4. Use launch-after-install if desired.

The installer is designed for per-user installation and should not require administrator rights.

## Upgrade
Close Echo, back up important audio/profile data, run the new installer, launch Echo and confirm the existing library, playlists, artwork, lyrics and settings remain available before deleting backups. The documented app identity remains `echo-desktop` and stable origin `http://127.0.0.1:43127`.

## Uninstall
Use Windows Settings > Apps or the Echo uninstall entry. The installer is designed to remove program files without deleting the Echo profile/library. The project owner reported a successful uninstall-preservation check on 15 November 2026; see `TEST_LOG.md`. Keep independent backups regardless.

## Optional lyric aligner
The Start Menu helper installs the optional local environment `.echo-lyric-venv` using 64-bit Python and verifies faster-whisper and lyric-align. Setup log: `Echo-Lyric-Aligner-Setup.log`. Normal playback and manual/provider lyrics do not require Python.

## Signing and safety
The 1.10.0 installer is unsigned. Windows may show an unknown-publisher/SmartScreen warning. A code-signing certificate is required for verified publisher identity. Do not disable Windows security to run an installer.

## Troubleshooting
- If node/npm is not recognised, install Node.js and reopen the terminal.
- If build fails, read terminal output and resolve the reported dependency/network issue.
- If library data appears missing, do not clear app/site data; check backups first.
- If lyric setup fails, inspect `Echo-Lyric-Aligner-Setup.log`.

