# XIVLauncher for Linux (AppImage)

A portable AppImage build of [XIVLauncher](https://github.com/goatcorp/FFXIVQuickLauncher) for Linux, designed to make launching **Final Fantasy XIV** easier without needing the official launcher.

This version was built and tested on **Linux Mint 22**, but it should run on any recent Linux distribution with basic dependencies.

---

## 🐧 What Is This?

This AppImage is a portable, standalone version of XIVLauncher for Linux users.

- ✅ No need to compile
- ✅ No root install
- ✅ Just download, `chmod +x`, and run!

---

## 🚀 Getting Started

### 1. **Download the AppImage**

```bash
wget https://github.com/meownoirsoft/xivlauncher-linux/releases/latest/download/XIVLauncher-x86_64.AppImage
```

### 2. Make it executable

```bash
chmod +x XIVLauncher-x86_64.AppImage
```

### 3. Run it

```bash
./XIVLauncher-x86_64.AppImage
```

First-time setup may take a few minutes as the launcher configures itself and downloads necessary files.

### 4. (Optional) Desktop File

A desktop entry file (`XIVLauncher.Core.desktop`) is included for easy launching from your desktop or applications menu. To use it:

```bash
cp XIVLauncher.Core.desktop ~/Desktop/
```

**Note:** The desktop file uses `$HOME` which will automatically expand to your home directory. If you placed the AppImage in a different location, edit the desktop file and replace `$HOME` with the actual path to where you stored the AppImage.

---

### ⚙️ Requirements

🎮 Steam version of FFXIV (optional but recommended)

✅ Vulkan drivers

✅ aria2 installed (for faster patching):

```bash
sudo apt install aria2
```

---

### 🧯 Troubleshooting

❗️"An error occurred trying to start process 'aria2c'"

Install aria2:

```bash
sudo apt install aria2
```

Or disable it in: Settings > Application > Use aria2 for patching.

❗️"DirectX 11 crashes or blank screen"

Make sure you're using the latest Proton-GE via Steam or use Wine with DXVK and Vulkan support.

You can also launch with:

```bash
PROTON_USE_WINED3D=1 ./XIVLauncher-x86_64.AppImage
```

For testing graphics backend differences.

❗️"RPC service crashes" (or launcher doesn't open)

Ensure libfuse2 is installed:

```bash
sudo apt install libfuse2
```

Or try launching with `--no-sandbox`

❗️AppImage doesn't run

Try these:

```bash
chmod +x XIVLauncher-x86_64.AppImage
./XIVLauncher-x86_64.AppImage
```

Or:

```bash
./XIVLauncher-x86_64.AppImage --appimage-extract
```

---

## 🛠 Build Information

- Built from: [XIVLauncher.Core](https://github.com/goatcorp/XIVLauncher.Core)
- Target Framework: .NET 8.0
- Platform: Linux x86_64
- Dalamud: Automatically fetches latest version (currently 14.0.1.0)

### Build Instructions (for devs)

Want to build your own?

- Clone the source repo
- Build with dotnet publish
- Place binaries inside XIVLauncher.AppDir/usr/bin
- Add .desktop file and run.sh
- Use appimagetool to package:

```bash
./appimagetool-x86_64.AppImage XIVLauncher.AppDir
```

---

## ❤️ Credit

- Based on the amazing work by [goatcorp/FFXIVQuickLauncher](https://github.com/goatcorp/FFXIVQuickLauncher)
- Linux support enhanced by squirrel-labs
- This AppImage build maintained by @meownoirsoft

---

## 📬 Feedback & Issues

Please open an issue if you encounter bugs, compatibility problems, or need help. PRs welcome if you want to help improve Linux support or automate the build process.

---

## 🎮 Enjoy the game, Warrior of Light!
