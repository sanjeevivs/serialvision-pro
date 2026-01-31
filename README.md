# SerialVision Pro

A professional-grade serial terminal and data analyzer available as both a **web application** and **desktop application**. SerialVision Pro combines the functionality of a traditional serial monitor, data plotter, and protocol analyzer into a single, modern interface.

## 🎯 **Available Versions**

### 🌐 **Web Version (PWA)**
- **Access**: Use directly in your browser
- **Features**: Full functionality via Web Serial API
- **Installation**: Installable as Progressive Web App

### 🖥️ **Desktop Version (Windows)**
- **Platform**: Windows 10/11 (64-bit)
- **Features**: Enhanced hardware access, native performance
- **Installation**: One-click installer or portable version
- **Download**: [Latest Release](https://sanjeevivs.github.io/serialvision-pro/)

## 📥 **Quick Download**

### Windows Desktop App:
[![Download for Windows](https://img.shields.io/badge/Download-Windows_Installer-00d4aa?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/sanjeevivs/serialvision-pro/releases/latest/download/SerialVision-Pro-Setup.exe)

## 🚀 **Features**

### **Core Communication**
- **Direct Serial Access**: Connect to Arduino, ESP32, Raspberry Pi via USB
- **Full-Duplex Communication**: Simultaneous send/receive without data loss
- **Configurable Baud Rates**: 300 to 921,600 baud
- **Break Signal & DTR/RTS Control**: Professional serial line control
- **Automatic Port Detection**: Lists all available serial ports

### **Data Visualization**
- **Real-time Plotting**: Automatic numeric value extraction from any data stream
- **Multi-Channel Support**: Visualize up to 3 data streams simultaneously
- **Anomaly Detection**: Statistical outlier detection with configurable thresholds
- **Hex Viewer**: Binary data visualization with ASCII side-by-side display
- **Spectrogram**: Frequency-domain representation of serial data

### **Professional Workflow**
- **Keyboard Macros**: Programmable function keys (F1-F12) for common commands
- **Session Persistence**: Save/load complete sessions with all data
- **Multi-Format Export**: CSV, JSON, and chart image exports
- **Performance Monitoring**: Live FPS, memory usage, and timing statistics
- **Auto-scrolling Terminal**: Configurable buffer limits (up to 2000 lines)

## 📦 **Installation**

### **Desktop App (Windows)**
1. **Download** the installer from the [Landing page](https://sanjeevivs.github.io/serialvision-pro/)
2. **Run** `SerialVision-Pro-Setup.exe`
3. **Follow** the installation wizard
4. **Launch** from Start Menu or desktop shortcut


## 🎮 **Getting Started**

### **1. Connect Your Device**
- Connect your microcontroller (Arduino, ESP32, etc.) via USB
- SerialVision Pro will automatically detect available ports
- Select your device from the port list

### **2. Configure Connection**
- **Baud Rate**: Match your device's configuration (commonly 115200 or 9600)
- **Parser**: Choose auto-detect, CSV, or space-separated
- **Enable Features**: Turn on auto-plotting and anomaly detection as needed

### **3. Start Debugging**
- **Terminal View**: Monitor incoming data with timestamps
- **Plotter View**: Real-time visualization of numeric values
- **Hex View**: Analyze binary data streams
- **Export Data**: Save sessions as CSV/JSON for further analysis

## 🔧 **Development**

### **Prerequisites**
- Node.js 18+ and npm
- Git
- Windows 10/11 for desktop builds

## 📊 **Version Comparison**

| Feature | Desktop Version | Web Version |
|---------|----------------|-------------|
| **Installation** | Native installer | Browser/PWA |
| **Hardware Access** | Direct via Node SerialPort | Web Serial API |
| **Offline Use** | Full functionality | Limited by PWA |
| **Performance** | Native performance | Browser sandboxed |
| **Updates** | Manual/GitHub Releases | Automatic via service worker |
| **Platform** | Windows only | Any browser platform |

## 🚨 **Troubleshooting**

### **Common Issues**

#### **Device Not Detected**
- **Check drivers**: Some USB-to-serial chips (CH340, CP2102) need drivers
- **Try different USB port**: Some ports may not provide enough power
- **Restart application**: Sometimes required for port detection

#### **Data Display Issues**
- **Baud rate mismatch**: Ensure device and terminal use same baud rate
- **Encoding issues**: Application uses UTF-8 by default
- **Line endings**: Check if device sends CR, LF, or CRLF

#### **Desktop App Issues**
- **Windows SmartScreen**: Click "More info" then "Run anyway" for first launch
- **Antivirus false positives**: Files are open source and safe
- **Permission errors**: Run as administrator if needed

## 🔒 **Security & Verification**

### **Download Verification**
```bash
# Verify SHA256 checksum on Windows
certutil -hashfile "SerialVision-Pro-Setup.exe" SHA256

# Compare with checksum in release notes
Expected SHA256: [CHECKSUM FROM RELEASE]
```

### **Code Transparency**
- **No Telemetry**: Application doesn't collect user data
- **Local Storage**: All data stays on your machine

## 📄 **License**

SerialVision Pro is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

**You are free to:**
- Use commercially
- Modify and distribute
- Use privately
- Sublicense

**Under the conditions:**
- Include original copyright notice
- Include license text in distributions

## 📞 **Support**

### **Get Help**
- **Documentation**: This README and landing page
- **Community**: Share your projects and tips

### **Planned future Features**
- [ ] macOS and Linux desktop versions
- [ ] Mobile support (serial over Bluetooth)
- [ ] Plugin system for custom protocols
- [ ] Cloud sync between versions
- [ ] VS Code extension

### **Current Focus**
- **Stability**: Bug fixes and performance improvements
- **Documentation**: Comprehensive guides and tutorials
- **Community**: Building user base and collecting feedback

---

**SerialVision Pro** demonstrates how modern web technologies can replace specialized desktop tools while improving accessibility and user experience. Whether you choose the web version for convenience or the desktop version for power, you get the same professional-grade serial terminal experience.

⭐ **Star this repo** if you find it useful!  
🐛 **Report issues** to help improve the project  
🔄 **Stay updated** by watching the repository  

