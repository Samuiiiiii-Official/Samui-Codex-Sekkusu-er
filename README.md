# Samui Codex Sekkusu-er

A native Windows 11 taskbar companion for checking your Codex usage limits.

## Features

- Remaining usage shown in the taskbar and notification area.
- Weekly and five-hour limits displayed with concentric progress rings. Pro accounts show the weekly limit.
- Local reset times, update status, and manual refresh.
- Light, dark, and system themes with animated backgrounds and subtle ring highlights.
- English, Japanese, and Simplified Chinese. English is the default; language changes are saved automatically.
- Optional Windows startup and automatic reconnection.
- Reduced-motion and high-contrast support.

## Requirements

- Windows 11, 64-bit.
- Codex CLI installed and signed in.
- PowerShell 7 for the optional install and uninstall scripts.

The application includes its desktop runtimes. Keep all files in the downloaded folder together.

## Download and run

1. Download `Samui-Codex-Sekkusu-er-0.1.0-win-x64.zip` from [Releases](https://github.com/Samuiiiiii-Official/Samui-Codex-Sekkusu-er/releases/latest).
2. Extract the ZIP to a folder.
3. Run `SamuiCodexSekkusuer.exe`.

Click the taskbar widget or tray icon to open the usage panel. Click outside it or press **Escape** to close it.

For a per-user installation, open PowerShell in the extracted folder and run:

```powershell
pwsh -NoProfile -File .\Install-Local.ps1
```

The installer adds a Start menu shortcut and enables startup at Windows sign-in. Administrator access is not required. Quit the application before installing an update.

## Settings

Open **Settings and more** in the usage panel to change the language, theme, animation, taskbar visibility, or startup preference.

If the taskbar widget is unavailable, use the tray icon. **Reattach to taskbar** retries placement. Version 0.1.0 supports the primary taskbar; placement depends on the available space and Windows shell behavior.

If a connection is interrupted, the last known reading remains visible and is marked as awaiting an update. Missing usage data is never shown as a zero balance.

Settings and cached readings are stored under `%LOCALAPPDATA%\Samui Codex Sekkusu-er`.

## Uninstall

Quit the application, then run:

```powershell
pwsh -NoProfile -File .\Uninstall-Local.ps1
```

Settings and logs are preserved. Add `-PurgeData` to remove them as well.

## Notices

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for dependency and attribution information. The SAMUI artwork retains its original copyright.

