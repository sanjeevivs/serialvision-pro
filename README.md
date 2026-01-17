# SerialVision Pro

A professional-grade serial terminal and data analyzer available as both a **web application** and **desktop application**. SerialVision Pro combines the functionality of a traditional serial monitor, data plotter, and protocol analyzer into a single, modern interface.

## 🎯 **Available Versions**

### 🌐 **Web Version (PWA)**
- **Access**: Use directly in your browser
- **Features**: Full functionality via Web Serial API
- **Installation**: Installable as Progressive Web App
- **URL**: [https://yoursanjeevivs.github.io/serialvision-pro](https://yoursanjeevivs.github.io/serialvision-pro)

### 🖥️ **Desktop Version (Windows)**
- **Platform**: Windows 10/11 (64-bit)
- **Features**: Enhanced hardware access, native performance
- **Installation**: One-click installer or portable version
- **Download**: [Latest Release](https://github.com/yoursanjeevivs/serialvision-pro/releases/latest)

## 📥 **Quick Download**

### Windows Desktop App:
[![Download for Windows](https://img.shields.io/badge/Download-Windows_Installer-00d4aa?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/yoursanjeevivs/serialvision-pro/releases/latest/download/SerialVision-Pro-Setup.exe)
[![Download Portable](https://img.shields.io/badge/Portable_Version-21262d?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/yoursanjeevivs/serialvision-pro/releases/latest/download/SerialVision-Pro-Portable.exe)


## 🚀 **Features**

### **Core Communication**
- ✅ **Direct Serial Access**: Connect to Arduino, ESP32, Raspberry Pi via USB
- ✅ **Full-Duplex Communication**: Simultaneous send/receive without data loss
- ✅ **Configurable Baud Rates**: 300 to 921,600 baud
- ✅ **Break Signal & DTR/RTS Control**: Professional serial line control
- ✅ **Automatic Port Detection**: Lists all available serial ports

### **Data Visualization**
- ✅ **Real-time Plotting**: Automatic numeric value extraction from any data stream
- ✅ **Multi-Channel Support**: Visualize up to 3 data streams simultaneously
- ✅ **Anomaly Detection**: Statistical outlier detection with configurable thresholds
- ✅ **Hex Viewer**: Binary data visualization with ASCII side-by-side display
- ✅ **Spectrogram**: Frequency-domain representation of serial data

### **Professional Workflow**
- ✅ **Keyboard Macros**: Programmable function keys (F1-F12) for common commands
- ✅ **Session Persistence**: Save/load complete sessions with all data
- ✅ **Multi-Format Export**: CSV, JSON, and chart image exports
- ✅ **Performance Monitoring**: Live FPS, memory usage, and timing statistics
- ✅ **Auto-scrolling Terminal**: Configurable buffer limits (up to 2000 lines)

## 📦 **Installation**

### **Desktop App (Windows)**
1. **Download** the installer from the [Releases page](https://github.com/sanjeevivs/serialvision-pro/releases)
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

## 🛠️ **Technical Architecture**

### **Desktop Version (Electron)**
```
Electron + Vue.js + Node SerialPort
├── Main Process: Native system integration
├── Renderer Process: Vue.js application
├── Preload Scripts: Secure IPC bridge
└── Native Modules: Direct hardware access
```

### **Web Version (PWA)**
```
Vue.js + Web Serial API + Chart.js
├── Service Worker: Offline functionality
├── Web Serial API: Hardware communication
├── IndexedDB: Local data storage
└── Vuetify 3: Material Design UI
```

## 📁 **Project Structure**
```
serialvision-pro/
├── docs/                    # GitHub Pages landing page
├── dist-windows/           # Windows desktop builds
├── index.html             # Main application
├── manifest.json          # PWA configuration
├── README.md              # This file
└── package.json           # Electron configuration
```

## 🔧 **Development**

### **Prerequisites**
- Node.js 18+ and npm
- Git
- Windows 10/11 for desktop builds

### **Build Desktop Version**
```bash
# Clone repository
git clone https://github.com/yoursanjeevivs/serialvision-pro.git
cd serialvision-pro

# Install dependencies
npm install

# Build for Windows
npm run build:win

# Output: dist-windows/SerialVision-Pro-Setup.exe
```

### **Run in Development**
```bash
# Web version (local server)
python -m http.server 8000
# Visit http://localhost:8000

# Desktop version (Electron)
npm start
```

## 📊 **Version Comparison**

| Feature | Desktop Version | Web Version |
|---------|----------------|-------------|
| **Installation** | Native installer | Browser/PWA |
| **Hardware Access** | Direct via Node SerialPort | Web Serial API |
| **Offline Use** | ✅ Full functionality | ✅ Limited by PWA |
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
- **Open Source**: MIT licensed, inspect all code

## 🤝 **Contributing**

We welcome contributions! Here's how:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### **Development Guidelines**
- Follow existing code style and patterns
- Test changes on both web and desktop versions
- Update documentation for new features
- Keep platform-specific code isolated

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

## 🌟 **Acknowledgements**

### **Built With**
- [Vue.js](https://vuejs.org/) - Progressive JavaScript Framework
- [Electron](https://www.electronjs.org/) - Cross-platform desktop apps
- [Chart.js](https://www.chartjs.org/) - Simple yet flexible JavaScript charting
- [Vuetify](https://vuetifyjs.com/) - Material Design Component Framework
- [Web Serial API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Serial_API) - Modern browser hardware access

---

## 📈 **Project Roadmap**

### **Planned Features**
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

