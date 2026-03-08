# XIVLauncher for Linux (AppImage)

A portable AppImage distribution of XIVLauncher that allows Linux users to run Final Fantasy XIV without needing the official launcher or compiling the project themselves.

This repository provides prebuilt AppImage releases for convenience and portability across modern Linux distributions.

---

## Why This Exists

Running XIVLauncher on Linux typically requires compiling the project manually and configuring dependencies. It is a nightmare.

For many users this creates friction.

This project packages the launcher as a **portable AppImage**, allowing users to simply download and run the application with minimal setup.

### Benefits:

- No compilation required
- No root installation required
- Works across most modern Linux distributions

---

## What This Provides

• Prebuilt AppImage releases of XIVLauncher  
• Portable launcher distribution for Linux users  
• Simplified installation process for Final Fantasy XIV players  

The AppImage can be downloaded and executed directly without modifying system packages.

---

## Quick Start

### Download

```bash
wget https://github.com/meownoirsoft/xivlauncher-linux/releases/latest/download/XIVLauncher-x86_64.AppImage
# Make executable
chmod +x XIVLauncher-x86_64.AppImage
# Run
./XIVLauncher-x86_64.AppImage
```

On first launch the launcher may download additional files and configure itself.

# Optional Desktop Integration

A desktop entry file is included for launching from your desktop environment.

```cp XIVLauncher.Core.desktop ~/Desktop/```

If the AppImage is stored in a different directory, edit the desktop file and update the path.

# Requirements

### Recommended environment:

Steam version of Final Fantasy XIV
Vulkan-compatible GPU drivers
Optional dependency for faster patching:
```
sudo apt install aria2
```

### Troubleshooting
aria2 not found

### Install aria2:

```sudo apt install aria2```

Or disable it in launcher settings.

### DirectX 11 crash or blank screen

Ensure you're using:
- Proton-GE via Steam
- Wine with DXVK and Vulkan support

Alternative launch option:

```PROTON_USE_WINED3D=1 ./XIVLauncher-x86_64.AppImage```
Launcher fails to start

Ensure libfuse2 is installed:

```sudo apt install libfuse2```
AppImage fails to run

Try:

```
chmod +x XIVLauncher-x86_64.AppImage
./XIVLauncher-x86_64.AppImage
```

Or extract manually:

```
./XIVLauncher-x86_64.AppImage --appimage-extract
```

### Build Information

Built from:

XIVLauncher.Core

Environment:

.NET 8.0

Linux x86_64

Dalamud plugins are automatically fetched by the launcher.

### Building the AppImage

Developers can reproduce the build with the following steps.

Clone the upstream repository

Build the launcher:

dotnet publish

Place binaries into the AppDir:

XIVLauncher.AppDir/usr/bin

Package using appimagetool:

./appimagetool-x86_64.AppImage XIVLauncher.AppDir
Credits

This project builds upon the work of several upstream projects:

- goatcorp/FFXIVQuickLauncher
- squirrel-labs Linux support

This AppImage packaging is maintained by @meownoirsoft. I will typically update this repo within a few days of a new update to Dalamud or other deps.

### Feedback and Contributions
Issues and pull requests are welcome.
If you encounter compatibility problems or want to help automate the build pipeline, feel free to open an issue.

Enjoy the game, Warrior of Light.
