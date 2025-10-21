# OUI-SPY

![OUI-SPY](ouispy.png)

**ESP32-S3 based BLE detection system with integrated buzzer and power management.**

This board has sick PCB art. Available on [Tindie](https://www.tindie.com) and [colonelpanic.tech](https://colonelpanic.tech) — ready to use, no additional components required.

---

## OUIs

Looking for manufacturer prefixes?  
👉 **Check the full list here:** [OUI List (`ouis.md`)](https://github.com/colonelpanichacks/ouispy-detector/blob/main/ouis.md)  
Gotta catch ’em all — contribute your findings!

If you need to verify an OUI, use one of these lookup tools:

- **Official IEEE OUI Lookup:** [https://standards.ieee.org/products-services/regauth/oui/index.html](https://standards.ieee.org/products-services/regauth/oui/index.html)
- **Alternate OUI Lookup:** [https://macaddress.io/](https://macaddress.io/)

---

## Firmware Options

Choose the firmware that matches your use case:

### [OUI-SPY Detector](https://github.com/colonelpanichacks/ouispy-detector)

**Multi-target BLE device scanner with OUI filtering**

- Detects multiple devices simultaneously by MAC address or manufacturer OUI
- Web-based configuration portal for target management
- Smart cooldown system prevents alert spam
- Audio feedback with different beep patterns for new vs. re-detected devices
- Persistent configuration storage
- Good for general surveillance and device monitoring

**Use Cases:** Security monitoring, device inventory, general BLE scanning

---

### [OUI-SPY Foxhunter](https://github.com/colonelpanichacks/ouispy-foxhunter)

**Precision proximity tracker for radio direction finding**

- Single target MAC address tracking with real-time RSSI analysis
- Variable proximity beeping based on signal strength (closer = faster beeps)
- Optimized for directional antenna usage and triangulation
- Aggressive scanning parameters for maximum sensitivity
- Clean audio feedback system for field operations

**Use Cases:** Radio direction finding, asset tracking, security device location, RF analysis

---

### [OUI-SPY UniPwn](https://github.com/colonelpanichacks/Oui-Spy-UniPwn)

**Advanced Unitree robot research tools with web interface**

- BLE-related research utilities and automation
- Real-time BLE scanning with signal strength indicators and target management
- Web interface with operations logging and system monitoring

**Use Cases:** Security research, authorized penetration testing, educational robotics security assessment

---

### [Flock You](https://github.com/colonelpanichacks/flock-you)

**Advanced surveillance device detection system**

- Multi-method detection using WiFi promiscuous mode and BLE scanning
- Real-time monitoring with comprehensive JSON output and audio alerts
- MAC address filtering and SSID pattern matching for surveillance devices
- Channel hopping across all 13 WiFi channels for maximum coverage
- Smart audio alert system with boot sequence, detection alerts, and heartbeat

**Use Cases:** Surveillance detection, privacy protection, security assessment, research and education

---

### [Sky-Spy](https://github.com/colonelpanichacks/Sky-Spy)

**Drone RemoteID detection and real-time mapping system**

- Dual-protocol scanning: WiFi promiscuous mode + BLE for RemoteID
- Real-time GPS coordinate extraction from drone broadcasts (location, altitude, speed, heading)
- Operator/pilot location tracking and identification
- JSON serial output for mapper integration
- Thread-safe audio alerts and multi-drone tracking

**Use Cases:** Drone detection, airspace monitoring, RemoteID compliance verification, counter-UAS awareness

---

## 3D Prints

Enhance your OUI-SPY with custom 3D printed cases and accessories:

- **OUI-SPY Case with External Antenna Hole** — Protective case with external antenna hole for enhanced RF performance and secure fit with ventilation.
- **OUI-SPY Travel Case** — Compact travel case for portable OUI-SPY operations, easy access to controls and indicators.
- **OUI-SPY Keychain** — Portable keychain case for everyday carry and discreet operations.
- **Mini Yagi Case** — Specialized case for directional antenna operations and foxhunting.
- **OUI-SPY SMA Spacer** — SMA connector spacer for external antenna mounting and better antenna positioning.

(Links available on the project page and model repositories; search for OUI-SPY prints to find creator uploads.)

---

## Hardware Specifications

- **MCU:** ESP32-S3 dual-core processor  
- **Connectivity:** WiFi 802.11n, Bluetooth 5.0, BLE  
- **Audio:** Integrated buzzer with PWM control  
- **Power:** USB-C powered with efficient power management  
- **Antenna:** Built-in antenna with option for external directional antenna  
- **Form Factor:** Compact PCB design optimized for portable use

---

## Quick Start

1. **Purchase** your OUI-SPY board from the store links above.  
2. **Choose firmware** from the repositories listed in the Firmware Options section.  
3. **Flash firmware** using PlatformIO or Arduino IDE.  
4. **Power on** and connect to WiFi AP `snoopuntothem`.  
5. **Configure targets** via web portal at `http://192.168.4.1`.

---

## Technical Features

### Advanced BLE Scanning
- Aggressive scanning parameters for optimal detection
- Dual-core processing for concurrent web interface and scanning
- Real-time RSSI analysis and signal strength reporting
- Support for both active and passive scanning modes

### Privacy & Security
- MAC address randomization for stealth operation
- Local processing — no cloud dependencies required
- Secure web configuration with timeout protection

### Audio System
- Multiple beep patterns for different alert types
- Variable frequency proximity indication
- Clean startup and ready signals
- Non-overlapping audio sequencing

---

## Contributing OUIs

We welcome contributions! Please add OUIs only to the dedicated file linked above:  
👉 [Add or View OUIs Here](https://github.com/colonelpanichacks/ouispy-detector/blob/main/ouis.md)

### How to Contribute

1. **Fork the repository** on [GitHub](https://github.com/colonelpanichacks/ouispy-detector).  
2. **Edit `ouis.md`** (the dedicated OUIs file).  
3. **Verify each OUI** using the official IEEE lookup or a trusted alternate.  
4. **Follow the format**: only include the prefix (first 3 bytes) in uppercase, e.g., `AA:BB:CC`.  
5. **Submit a Pull Request** with a short note about the source/verification.

Gotta catch ’em all — add your OUIs and help make surveillance detection better for everyone!

---

## License

Open source project. Hardware available commercially via the project store links.

---
