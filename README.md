# xdBot - iOS Support Edition

<p align="center">
  <img src="logo.png" alt="xdBot Logo" width="200"/>
</p>

<p align="center">
  <strong>Geometry Dash simple and easy to use botting tool - Now with iOS Support!</strong>
</p>


## 🚀 What's New - iOS Support!

xdBot now supports iOS devices! Experience the full power of xdBot automation on your iPhone and iPad.

### ✨ iOS Features
- **Touch Controls**: Optimized touch-based interface for iOS devices
- **Gesture Sensitivity**: Adjustable sensitivity for precise control
- **ARM64 Architecture**: Native support for modern iOS devices
- **iOS 14.0+**: Compatible with iOS 14 and later versions
- **JIT Support**: Works on non-jailbroken devices

## 🎮 Features

### Core Functionality
- **Macro Recording & Playback**: Record your gameplay and replay it with precision
- **Multiple Accuracy Modes**: Vanilla, Input Fixes, Frame Fixes
- **Auto-Clicker**: Automated clicking with customizable settings
- **Clickbot**: Advanced bot functionality for level completion
- **Frame Stepper**: Step through frames for precise analysis

### Game Enhancements
- **TPS Bypass**: Unlock frame rate limitations
- **Layout Mode**: Enhanced level editing experience
- **Show Trajectory**: Visualize jump paths and trajectories
- **Coin Finder**: Locate coins in levels easily
- **Speedhack**: Adjust game speed for practice

### Practice Mode Fixes
- **Input Handling**: Improved input responsiveness
- **Player Behavior**: Enhanced player mechanics
- **Play Layer**: Optimized gameplay experience

## 📱 Platform Support

| Platform |     Status      | Architecture |
|----------|-----------------|--------------|
|  **iOS** | ✅ **Building** | ARM64 |

## 🛠️ Installation

### iOS Installation

1. **Install Geode Launcher** on your iOS device
2. **Download** the latest `xdBot.geode` file from [Releases](https://github.com/ZiLko/xdBot/releases)
3. **Transfer** the file to your device via:
   - Web Server (recommended): `http://[device-ip]:8080`
   - iTunes/Finder file sharing
4. **Launch** Geometry Dash and enjoy!

### Other Platforms

Download the appropriate `.geode` file for your platform from the [Releases](https://github.com/ZiLko/xdBot/releases) page.

## 🔧 Building from Source

### iOS Build Requirements
- **macOS** with Xcode installed
- **Geode SDK** 4.4.0 or higher
- **iOS SDK** (included with Xcode)

### Quick Build
```bash
# Clone the repository
git clone https://github.com/ZiLko/xdBot.git
cd xdBot

# Build for iOS
chmod +x build_macos.sh
./build_macos.sh
```

### Manual Build
```bash
# Install Geode CLI and SDK
geode sdk install
geode sdk install-binaries --platform ios

# Build
cmake -B build-ios -DCMAKE_SYSTEM_NAME=iOS -DGEODE_TARGET_PLATFORM=iOS
cmake --build build-ios
```

For detailed build instructions, see:
- [macOS Build Guide](BUILD_MACOS_GUIDE.md)
- [Build Structure](iOS_BUILD_STRUCTURE.md)
- [Step-by-Step Setup](STEP_BY_STEP_SETUP.md)

## ⚙️ Configuration

### iOS-Specific Settings
- **iOS Touch Controls**: Enable touch-based interface
- **iOS Gesture Sensitivity**: Adjust gesture responsiveness (0.1-3.0)
- **Frame Fixes Limit**: Optimize performance for iOS devices

### General Settings
- **Macro Accuracy**: Choose between Vanilla, Input Fixes, or Frame Fixes
- **Frame Offset**: Fine-tune macro timing (-8 to +8 frames)
- **Auto Settings**: Auto-stop playing, auto-disable speedhack
- **File Paths**: Customize macro, autosave, and render locations

## 🎯 Usage

### Recording Macros
1. Open the xdBot menu in-game
2. Click "Record" to start recording
3. Play through your level
4. Stop recording when finished
5. Save your macro for later use

### Playing Macros
1. Load a previously recorded macro
2. Select your preferred accuracy mode
3. Click "Play" to execute the macro
4. Watch as xdBot replicates your gameplay

### iOS Touch Controls
- **Tap**: Primary interaction
- **Long Press**: Secondary actions
- **Swipe**: Navigate menus
- **Pinch**: Zoom (where applicable)

## 🔒 Security & Compatibility

### iOS Security
- **App Store Compliance**: Safe for non-jailbroken devices
- **Sandboxed**: Respects iOS security model
- **No System Modifications**: Works within Geode framework

### Compatibility
- **Geometry Dash**: Version 2.2074
- **iOS**: 14.0 and later
- **Geode**: 4.4.0 and later

## 🐛 Troubleshooting

### Common iOS Issues
- **Installation Failed**: Ensure Geode Launcher is properly installed
- **Mod Not Loading**: Check iOS version compatibility (14.0+)
- **Touch Controls**: Adjust gesture sensitivity in settings
- **Performance**: Lower frame fixes limit for older devices

### Support Resources
- [iOS Installation Guide](README_iOS.md)
- [Build Troubleshooting](BUILD_MACOS_GUIDE.md#troubleshooting)
- [Discord Community](https://discord.gg/w6yvdzVzBd)

## 📊 Changelog

### v2.4.1 - iOS Support Edition
- ✅ Added iOS platform support
- ✅ Implemented touch controls interface
- ✅ Added gesture sensitivity settings
- ✅ Optimized for ARM64 architecture
- ✅ iOS 14.0+ compatibility
- ✅ JIT-less support for non-jailbroken devices

### Previous Versions
- **v2.4.0**: Removed FFmpeg API dependency, bug fixes
- **v2.3.x**: Performance improvements, stability fixes
- **v2.2.x**: Enhanced macro system, UI improvements

## 🤝 Contributing

We welcome contributions! Please see our [contribution guidelines](CONTRIBUTING.md) for details.

### Development Setup
1. Fork the repository
2. Follow the [build instructions](#building-from-source)
3. Make your changes
4. Test on multiple platforms
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Geode SDK Team**: For the amazing modding framework
- **iOS Community**: For testing and feedback
- **Contributors**: Everyone who helped make iOS support possible

## 📞 Support

- **Discord**: [Join our community](https://discord.gg/w6yvdzVzBd)
- **GitHub Issues**: [Report bugs](https://github.com/ZiLko/xdBot/issues)
- **Documentation**: Check our [guides](FILES_LIST.md)

---

<p align="center">
  <strong>Experience the future of Geometry Dash automation on iOS!</strong>
</p>

<p align="center">
  Made with ❤️ by <a href="https://github.com/ZiLko">Zilko</a> and the iOS community
</p>
