# Hexapod Bluetooth Controller App

## 📱 Complete Android App for Hexapod Robot Control

A fully-functional Android application to control your hexapod robot via Bluetooth connection. Built with Kotlin and Material Design.

## 🚀 Quick Download APK

**Latest APK Build:** Ready for download
- Download link will be generated from GitHub Actions Releases
- Minimum Android: 5.0 (API 21)
- Target Android: 14 (API 34)
- Size: ~5-8 MB

## 📥 Installation Methods

### Method 1: Direct Download (Recommended)
Once GitHub Actions builds complete, download APK from:
```
https://github.com/kumarnukala05-eng/hexapod-controller/releases
```

### Method 2: Via ADB (USB)
```bash
adb install HexapodController-release.apk
```

### Method 3: Manual Installation
1. Download APK to your phone
2. Open Files/File Manager
3. Navigate to APK file
4. Tap to install
5. Grant permissions when prompted

## ✨ Features

✅ **Bluetooth Scanning** - Find and pair with ESP32 "CreepyPhantoms_Test"
✅ **Device Connection** - Secure RFCOMM socket connection
✅ **6-Button Control** - UP, DOWN, STOP, FWD, BACK, TURN
✅ **Connection Status** - Real-time indicator
✅ **Command Logging** - Monitor all sent commands
✅ **Material Design UI** - Modern, responsive interface
✅ **Thread-Safe Communication** - Stable Bluetooth handling
✅ **Auto-Reconnect** - Automatic reconnection on disconnect

## 🎮 Controls

| Button | Command | Action |
|--------|---------|--------|
| UP | 'U' | Lift leg (raise) |
| DOWN | 'D' | Lower leg |
| STOP | 'S' | Mid-height stance |
| FWD | 'F' | Forward walk |
| BACK | 'B' | Backward walk |
| TURN | 'T' | Turn in place |

## 📋 Requirements

- Android Device: API 21+ (Android 5.0+)
- Bluetooth 4.0+
- ESP32 with hexapod code running
- Bluetooth name: "CreepyPhantoms_Test"
- Baud rate: 115200

## 🔐 Permissions Required

- `BLUETOOTH` - Connect to devices
- `BLUETOOTH_ADMIN` - Manage connections
- `BLUETOOTH_CONNECT` - Android 12+
- `BLUETOOTH_SCAN` - Android 12+
- `ACCESS_FINE_LOCATION` - Bluetooth scanning

## 🛠️ Building from Source

Requirements:
- Android Studio (latest)
- Kotlin support enabled
- Android SDK 34
- JDK 11+

### Setup Steps:

1. Clone this repo:
```bash
git clone https://github.com/kumarnukala05-eng/hexapod-controller.git
cd hexapod-controller
```

2. Open in Android Studio:
```bash
open -a "Android Studio" .
```

3. Build APK:
```bash
./gradlew assembleRelease
```

4. Find APK at:
```
app/build/outputs/apk/release/app-release.apk
```

## 📱 How to Use

### First Time Setup:
1. Enable Bluetooth on your phone
2. Pair with "CreepyPhantoms_Test" in Settings
3. Install HexapodController APK
4. Open the app

### Using the App:
1. **SCAN** - Scans for paired Bluetooth devices
2. **SELECT** - Choose "CreepyPhantoms_Test" from list
3. **CONNECT** - Establish Bluetooth connection
4. **CONTROL** - Use buttons to move hexapod
5. Watch the **Command Log** for confirmation

### Connection Troubleshooting:
- Red status = Not connected
- Green status = Connected
- Check ESP32 is powered on
- Check Bluetooth is enabled
- Grant app permissions in Settings

## 📊 Technical Stack

- **Language:** Kotlin
- **Architecture:** MVVM Pattern
- **UI Framework:** Android XML Layout
- **Build System:** Gradle
- **Bluetooth:** RFCOMM Sockets
- **Threading:** Kotlin Coroutines
- **Target SDK:** Android 34 (API 34)
- **Min SDK:** Android 21 (API 21)

## 🔧 Project Structure

```
hexapod-controller/
├── app/
│   ├── src/main/
│   │   ├── kotlin/com/hexapod/controller/
│   │   │   ├── MainActivity.kt
│   │   │   ├── BluetoothManager.kt
│   │   │   └── CommandHandler.kt
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml
│   │   │   ├── values/
│   │   │   │   ├── colors.xml
│   │   │   │   └── strings.xml
│   │   │   └── drawable/
│   │   └── AndroidManifest.xml
│   ├── build.gradle.kts
│   └── proguard-rules.pro
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## 🚀 GitHub Actions - Automated APK Building

This repository includes GitHub Actions CI/CD that automatically:
- ✅ Compiles Kotlin code
- ✅ Resolves dependencies
- ✅ Signs APK with secure keystore
- ✅ Creates release artifacts
- ✅ Provides download link

View builds: [Actions Tab](https://github.com/kumarnukala05-eng/hexapod-controller/actions)

## 📥 APK Download Links

**After builds complete, download from:**

🔗 **[GitHub Releases](https://github.com/kumarnukala05-eng/hexapod-controller/releases)**

- HexapodController-release.apk (Signed, optimized)
- HexapodController-debug.apk (Debug version)
- Build logs and artifacts

## 🐛 Troubleshooting

### App crashes on startup
- Check permissions in Settings → Apps → HexapodController
- Grant Bluetooth permissions
- Reinstall if permissions not working

### Can't find ESP32 device
- Ensure ESP32 is powered on
- Check Bluetooth name is "CreepyPhantoms_Test"
- Restart ESP32 and phone Bluetooth
- Try pairing again in Settings

### Commands not sending
- Check connection status (should show green)
- Verify baud rate is 115200
- Check Serial Monitor on Arduino IDE
- Ensure ESP32 code is running

### Bluetooth disconnects frequently
- Reduce distance between phone and ESP32
- Check for WiFi/2.4GHz interference
- Update phone's Bluetooth drivers
- Use external antenna on ESP32

## 📞 Support

For issues or questions:
1. Check GitHub Issues tab
2. Review Serial Monitor logs
3. Verify Bluetooth permissions
4. Test with Serial Monitor first

## 📜 License

MIT License - Free for personal and educational use

## 🎉 Credits

Built for hexapod robot ESP32 control system.
Supports 6-legged robot with Bluetooth interface.

---

**Latest Build:** Check Actions tab for most recent APK
**Status:** ✅ Active Development
**Version:** 1.0.0
**Last Updated:** January 2026
