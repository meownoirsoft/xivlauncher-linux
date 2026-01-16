# XIVLauncher Core - Custom Build

This repository contains a custom build of XIVLauncher Core with the latest Dalamud version support.

## Files

- **XIVLauncher-x86_64.AppImage** - The main launcher executable (AppImage format for Linux)
- **XIVLauncher.Core.desktop** - Desktop entry file for easy launching

## Installation

1. Download the `XIVLauncher-x86_64.AppImage` file
2. Make it executable:
   ```bash
   chmod +x XIVLauncher-x86_64.AppImage
   ```
3. (Optional) Copy the desktop file to your desktop or applications directory:
   ```bash
   cp XIVLauncher.Core.desktop ~/Desktop/
   ```

## Usage

Simply run the AppImage:
```bash
./XIVLauncher-x86_64.AppImage
```

Or double-click it from your file manager if your system supports AppImages.

## Build Information

- Built from: [XIVLauncher.Core](https://github.com/goatcorp/XIVLauncher.Core)
- Target Framework: .NET 8.0
- Platform: Linux x86_64
- Dalamud: Automatically fetches latest version (currently 14.0.1.0)

## Notes

- The launcher will automatically download and use the latest compatible Dalamud version when launched
- First launch may take longer as Dalamud components are downloaded
- Make sure you have .NET runtime dependencies installed if needed

