# OUI-SPY

![OUI-SPY](ouispy.png)

**ESP32-S3 based BLE detection system with integrated buzzer and power management.**

This board has sick PCB art. Available on [Tindie](https://www.tindie.com) and [colonelpanic.tech](https://colonelpanic.tech) - Ready-to-use, no additional components required.

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
- Good for foxhunting competitions and asset recovery

**Use Cases:** Radio direction finding, asset tracking, security device location, RF analysis

---

### [OUI-SPY UniPwn](https://github.com/colonelpanichacks/Oui-Spy-UniPwn)

**Advanced Unitree robot exploitation system with web interface**

- BLE-based command injection exploits for Unitree Go2, G1, H1, and B2 robots
- AutoPwn automation with 7-step exploitation and bulletproof error handling
- Real-time BLE scanning with signal strength indicators and target management
- Custom command injection with SSID/password injection methods
- Comprehensive web interface with operations logging and system monitoring
- AES-CFB128 encryption implementation for Unitree's crypto protocol
- Based on original research by Bin4ry and d0tslash

**Use Cases:** Security research, authorized penetration testing, educational robotics security assessment

---

### [Flock You](https://github.com/colonelpanichacks/flock-you)

**Advanced Flock Safety surveillance camera detection system**

- Multi-method detection using WiFi promiscuous mode and BLE scanning
- Real-time monitoring with comprehensive JSON output and audio alerts
- MAC address filtering and SSID pattern matching for surveillance devices
- Channel hopping across all 13 WiFi channels for maximum coverage
- Smart audio alert system with boot sequence, detection alerts, and heartbeat
- Built-in datasets from deflock.me for enhanced detection accuracy

**Use Cases:** Surveillance detection, privacy protection, security assessment, research and education

---

### [Sky-Spy](https://github.com/colonelpanichacks/Sky-Spy)

**Drone RemoteID detection and real-time mapping system**

- Dual-protocol scanning: WiFi promiscuous mode + BLE for OpenDroneID (ASTM F3411)
- Real-time GPS coordinate extraction from drone broadcasts (location, altitude, speed, heading)
- Operator/pilot location tracking and identification
- JSON serial output for mesh-mapper.py visualization integration
- Thread-safe audio alerts: 3 quick beeps on detection, heartbeat every 5 seconds
- Multi-drone tracking: Monitor up to 8 drones simultaneously
- Non-blocking buzzer implementation with dedicated FreeRTOS task

**Use Cases:** Drone detection, airspace monitoring, RemoteID compliance verification, counter-UAS awareness

---

## Hardware Specifications

- **MCU:** ESP32-S3 dual-core processor
- **Connectivity:** WiFi 802.11n, Bluetooth 5.0, BLE
- **Audio:** Integrated buzzer with PWM control
- **Power:** USB-C powered with efficient power management
- **Antenna:** Built-in antenna with option for external directional antenna
- **Form Factor:** Compact PCB design optimized for portable use

## Quick Start

1. **Purchase** your OUI-SPY board from [Tindie](https://www.tindie.com) or [colonelpanic.tech](https://colonelpanic.tech)
2. **Choose firmware** from the repositories above
3. **Flash firmware** using PlatformIO or Arduino IDE
4. **Power on** and connect to WiFi AP `snoopuntothem`
5. **Configure targets** via web portal at `http://192.168.4.1`

## Technical Features

### Advanced BLE Scanning
- Maximum aggressive scanning parameters for optimal detection
- Dual-core processing for concurrent web interface and scanning
- Real-time RSSI analysis and signal strength reporting
- Support for both active and passive scanning modes

### Privacy & Security
- MAC address randomization for stealth operation
- No traceable hardware fingerprints
- Secure web configuration with timeout protection
- Local processing - no cloud dependencies

### Audio System
- Multiple beep patterns for different alert types
- Variable frequency proximity indication
- Clean startup and ready signals
- Non-overlapping audio sequencing

---

**Choose your firmware above and start detecting.**

## License

Open source project. Hardware available commercially on [Tindie](https://www.tindie.com) and [colonelpanic.tech](https://colonelpanic.tech).
