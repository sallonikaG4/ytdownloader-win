# YouTube to MP3 Downloader for Windows

A modern, desktop application for downloading YouTube videos and playlists and converting them to MP3 format at customizable quality (default: 172kbps).

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-GPL--3.0-green)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

## 🎯 Purpose

This application provides a **local, ad-free solution** for downloading YouTube content as MP3 files. Unlike browser-based solutions, this runs entirely on your computer with:

- ✅ **No ads or popups**
- ✅ **No browser required** (native Windows application)
- ✅ **No subscription fees**
- ✅ **Complete privacy** (all processing happens locally)
- ✅ **Playlist support** with selective downloading
- ✅ **Automatic handling** of unavailable/blocked videos

## ✨ Features

### Core Functionality
- 🎵 **Download Single Videos** - Convert any YouTube video to MP3
- 📁 **Download Entire Playlists** - Download complete playlists with automatic organization
- 🎯 **Selective Playlist Download** - Choose which videos to download from playlists
- 🚫 **Smart Filtering** - Automatically skips unavailable/blocked videos
- 🎚️ **Customizable Quality** - Choose from 128kbps to 320kbps (default: 172kbps)

### User Interface
- 🎨 **Modern, Tech-Savvy UI** - Beautiful dark theme with gradient accents
- 📊 **Real-time Progress** - Live download progress with speed and ETA
- 📂 **File Management** - Browse and access all downloaded files
- 🖥️ **Native Windows App** - No browser needed
- 📱 **Responsive Design** - Works on all screen sizes

### Technical Features
- 🚀 **Fast & Efficient** - Powered by yt-dlp and FFmpeg
- 🔒 **Privacy-First** - All processing happens locally
- 💾 **Persistent Settings** - Remembers your downloads folder preference
- 🔄 **Auto-Installation** - Installer includes FFmpeg setup
- 🎯 **Error Handling** - Graceful handling of unavailable content

## 📦 Installation

### Option 1: Installer (Recommended)

1. Download `YouTubeToMP3_Setup.exe` from the [Releases](https://github.com/sallonikaG4/ytdownloader-windows/releases) page
2. Run the installer
3. Follow the installation wizard
4. The installer will automatically set up FFmpeg if needed
5. Launch from Start Menu or desktop shortcut

### Option 2: Build from Source

See [BUILD_INSTRUCTIONS.md](BUILD_INSTRUCTIONS.md) for detailed instructions.

## 🚀 Usage

1. **Launch the application**
   - From Start Menu or desktop shortcut

2. **Select Downloads Folder** (First Launch)
   - Choose where you want downloaded files saved
   - Your choice will be remembered for future sessions

3. **Download a Video**
   - Paste a YouTube video URL in the input field
   - Click **"Get Info"** to preview the video
   - Adjust quality settings if needed (default: 172kbps)
   - Click **"Download & Convert"**
   - Watch real-time progress

4. **Download a Playlist**
   - Paste a YouTube playlist URL
   - Click **"Get Info"** to see all videos
   - **Select which videos** you want to download (use "Select All" or "Deselect All")
   - Unavailable/blocked videos are automatically excluded
   - Click **"Download & Convert"**

5. **Access Downloaded Files**
   - All downloaded MP3 files appear in the "Downloaded Files" section
   - Click "Download" to save a file to your default Downloads folder
   - Files are organized by playlist name (for playlists)

## 📁 Output Structure

- **Single Videos**: Saved directly to your chosen downloads folder
- **Playlists**: Organized in subfolders by playlist name, with tracks numbered:
  ```
  Documents/YouTube Downloads/
  ├── My Playlist Name/
  │   ├── 1 - Song Title.mp3
  │   ├── 2 - Another Song.mp3
  │   └── ...
  └── Single Video Title.mp3
  ```

## ⚙️ Configuration

### Default Settings
- **Bitrate**: 172kbps
- **Output Directory**: `Documents/YouTube Downloads`
- **Format**: MP3

### Available Bitrates
- 128kbps
- 172kbps (default)
- 192kbps
- 256kbps
- 320kbps

## 🔧 Requirements

- **Windows 10 or later**
- **FFmpeg** - Required for audio conversion (installer will set this up automatically)

## 🔧 Troubleshooting

### FFmpeg Not Found
- The installer should set up FFmpeg automatically
- If not, download from [FFmpeg.org](https://ffmpeg.org/download.html)
- Add FFmpeg to your system PATH
- Restart the application

### Application Won't Start
- Check Windows Defender or antivirus settings
- Ensure you have administrator rights if needed
- Check the Event Viewer for error details

### Download Fails
- Check your internet connection
- Verify the YouTube URL is correct
- Some videos may be region-restricted or unavailable (these are automatically skipped)

### Conversion Issues
- Ensure FFmpeg is properly installed
- Check that you have write permissions in the downloads folder
- Try selecting a different downloads folder

## 🏗️ Project Structure

```
.
├── youtube_downloader.py      # Core download logic
├── app.py                      # Flask web server
├── desktop_app.py             # Desktop application wrapper
├── templates/                 # HTML templates
├── static/                     # CSS and JavaScript
├── youtube_downloader.spec    # PyInstaller spec
├── build_installer.iss        # Inno Setup installer script
└── README.md                   # This file
```

## 🛠️ Development

### Running in Development Mode

```bash
# Install dependencies
pip install -r requirements.txt

# Start Flask server
python app.py

# Or run desktop app
python desktop_app.py
```

Then open http://localhost:5000 in your browser (if using Flask directly).

### Building for Distribution

See [BUILD_INSTRUCTIONS.md](BUILD_INSTRUCTIONS.md) for detailed build instructions.

## 📝 Technical Details

### Technologies Used
- **Python 3.8+** - Core language
- **yt-dlp** - YouTube downloading engine
- **FFmpeg** - Audio conversion
- **Flask** - Web framework (for UI)
- **PyQt5** - Desktop application framework
- **PyInstaller** - Application bundling
- **Inno Setup** - Windows installer

### Architecture
- **Backend**: Flask REST API serving the web UI
- **Frontend**: Modern HTML/CSS/JavaScript
- **Desktop Wrapper**: PyQt5 WebEngine (embeds web UI in native window)
- **Download Engine**: yt-dlp with FFmpeg post-processing

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🛡️ Legal Notice

This tool is for **personal use only**. Please respect:
- YouTube's Terms of Service
- Copyright laws
- Content creators' rights

**Only download content you have permission to download.**

## 📄 License

This project is licensed under the **GNU General Public License v3.0** - see the [LICENSE](LICENSE) file for details.

## 🙏 Credits

- **yt-dlp** - [GitHub](https://github.com/yt-dlp/yt-dlp) - YouTube downloading engine
- **FFmpeg** - [FFmpeg.org](https://ffmpeg.org/) - Audio/video processing
- **Flask** - [Flask.palletsprojects.com](https://flask.palletsprojects.com/) - Web framework
- **PyQt5** - [Riverbank Computing](https://www.riverbankcomputing.com/software/pyqt/) - GUI framework
- **Inter Font** - [Google Fonts](https://fonts.google.com/specimen/Inter) - Typography

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/sallonikaG4/ytdownloader-windows/issues)
- **Releases**: [GitHub Releases](https://github.com/sallonikaG4/ytdownloader-windows/releases)

---

**Made with ❤️ for Windows users who want a simple, ad-free way to enjoy YouTube content offline.**

**Enjoy your music! 🎵**

