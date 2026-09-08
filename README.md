# Samui Codex Sekkusu-er

A native Windows taskbar companion for checking your Codex usage limits and credits balance.

## Features

- Remaining usage shown in the taskbar and notification area.
- Weekly and five-hour limits displayed with concentric progress rings. Pro accounts show the weekly limit.
- Local reset times, update status, and manual refresh.
- Purchased credits balance, displayed separately from periodic usage limits.
- Light, dark, and system themes with animated backgrounds and subtle ring highlights.
- English, Japanese, and Simplified Chinese. English is the default; language changes are saved automatically.
- Optional Windows startup and automatic reconnection.
- Reduced-motion and high-contrast support.

## Requirements

- Windows 10 version 2004 (build 19041) or later, including Windows 11; 64-bit.
- Codex CLI installed and signed in.
- PowerShell 7 for the optional install and uninstall scripts.

The application includes its desktop runtimes. Keep all files in the downloaded folder together.

## Download and run

1. Download `Samui-Codex-Sekkusu-er-0.2.0-win-x64.zip` from [Releases](https://github.com/Samuiiiiii-Official/Samui-Codex-Sekkusu-er/releases/latest).
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

If the taskbar widget is unavailable, use the tray icon. **Reattach to taskbar** retries placement. The widget supports the primary horizontal taskbar; vertical taskbars use the tray icon. Placement depends on the available space and Windows shell behavior.

If a connection is interrupted, the last known reading remains visible and is marked as awaiting an update. Missing usage data is never shown as a zero balance.

**Credits balance** shows the additional credits reported by Codex. It can show a numeric balance, unlimited credits, or unavailable data. It is separate from the number of available usage resets.

Windows 10 compatibility uses the documented platform API baseline and classic taskbar control types. Runtime testing for this release was performed on Windows 11; Windows 10 device validation remains pending.

## Release protection

Distributed application assemblies use symbol renaming, encrypted strings, integer encoding and control-flow transformations. Framework activation, interoperability and data-format contracts are preserved. These protections increase reverse-engineering effort; they do not make the program impossible to inspect or modify.

Settings and cached readings are stored under `%LOCALAPPDATA%\Samui Codex Sekkusu-er`.

## Uninstall

Quit the application, then run:

```powershell
pwsh -NoProfile -File .\Uninstall-Local.ps1
```

Settings and logs are preserved. Add `-PurgeData` to remove them as well.

## Notices

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for dependency and attribution information. The SAMUI artwork retains its original copyright.
