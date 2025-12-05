# How to Create a GitHub Release with the Windows Installer

## Step 1: Download the Artifact

1. Go to your repository: https://github.com/sallonikaG4/ytdownloader-windows
2. Click on the **"Actions"** tab
3. Find the latest successful workflow run (green checkmark)
4. Scroll down to the **"Artifacts"** section
5. Click **"Windows-Application"** to download the ZIP file
6. Extract the ZIP file - you'll find:
   - `YouTubeToMP3.exe` (standalone executable)
   - `YouTubeToMP3_Setup.exe` (Windows installer - **use this for release**)

## Step 2: Create a Release

1. Go to your repository: https://github.com/sallonikaG4/ytdownloader-windows
2. Click on **"Releases"** (on the right sidebar, or go to: https://github.com/sallonikaG4/ytdownloader-windows/releases)
3. Click **"Create a new release"** or **"Draft a new release"**

## Step 3: Fill in Release Details

**Tag version:**
- Click **"Choose a tag"** → Type: `v2.0.0` → Click **"Create new tag: v2.0.0 on publish"**

**Release title:**
```
YouTube to MP3 Downloader v2.0.0 for Windows
```

**Description:**
```markdown
## 🎉 YouTube to MP3 Downloader v2.0.0 for Windows

### ✨ Features
- 🎵 Download single videos or entire playlists
- 🎯 Select specific videos from playlists
- 🎨 Modern, tech-savvy user interface
- 📁 Choose your downloads folder on startup
- ⚡ Real-time download progress
- 🚫 Automatically skips unavailable/blocked videos
- 🖥️ Native Windows application (no browser needed)
- 🔄 Automatic FFmpeg installation support

### 📦 Installation
1. Download `YouTubeToMP3_Setup.exe`
2. Run the installer
3. Follow the installation wizard
4. The installer will automatically set up FFmpeg if needed
5. Launch from Start Menu or desktop shortcut

### ⚙️ Requirements
- Windows 10 or later
- FFmpeg (installer will set this up automatically)

### 📝 Notes
- Default bitrate: 172kbps (customizable)
- Downloads saved to: `Documents/YouTube Downloads`
- First launch will prompt you to select a downloads folder
- All Python dependencies are bundled - no need to install Python separately

### 🐛 Issues?
Please report issues on the [Issues](https://github.com/sallonikaG4/ytdownloader-windows/issues) page.
```

## Step 4: Upload the Installer

1. Scroll down to **"Attach binaries by dropping them here or selecting them"**
2. Drag and drop `YouTubeToMP3_Setup.exe` from the extracted ZIP
3. Wait for upload to complete

## Step 5: Publish

1. Make sure **"Set as the latest release"** is checked (if available)
2. Click **"Publish release"**

## Done! 🎉

Your release is now live! Users can download the installer from:
https://github.com/sallonikaG4/ytdownloader-windows/releases

---

**Quick Links:**
- Release page: https://github.com/sallonikaG4/ytdownloader-windows/releases
- Download installer: https://github.com/sallonikaG4/ytdownloader-windows/releases/latest (after publishing)

