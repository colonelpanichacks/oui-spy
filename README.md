# OUI-SPY

![OUI-SPY](ouispy.png)

**Professional ESP32-S3 based BLE detection system with integrated buzzer and power management.**

Available on [Tindie](https://www.tindie.com) - Ready-to-use, no additional components required.

## Firmware Options

Choose the firmware that matches your use case:

### 🔍 [OUI-SPY Detector](https://github.com/colonelpanichacks/ouispy-detector)

**Multi-target BLE device scanner with OUI filtering**

- Detects multiple devices simultaneously by MAC address or manufacturer OUI
- Web-based configuration portal for easy target management
- Smart cooldown system prevents alert spam
- Audio feedback with different beep patterns for new vs. re-detected devices
- Persistent configuration storage
- Perfect for general surveillance and device monitoring

**Use Cases:** Security monitoring, device inventory, general BLE scanning

---

### 🦊 [OUI-SPY Foxhunter](https://github.com/colonelpanichacks/ouispy-foxhunter)

**Precision proximity tracker for radio direction finding**

- Single target MAC address tracking with real-time RSSI analysis
- Variable proximity beeping based on signal strength (closer = faster beeps)
- Optimized for directional antenna usage and triangulation
- Aggressive scanning parameters for maximum sensitivity
- Clean audio feedback system for field operations
- Perfect for foxhunting competitions and asset recovery

**Use Cases:** Radio direction finding, asset tracking, security device location, RF analysis

---

## Hardware Specifications

- **MCU:** ESP32-S3 dual-core processor
- **Connectivity:** WiFi 802.11n, Bluetooth 5.0, BLE
- **Audio:** Integrated buzzer with PWM control
- **Power:** USB-C powered with efficient power management
- **Antenna:** Built-in antenna with option for external directional antenna
- **Form Factor:** Compact PCB design optimized for portable use

## Quick Start

1. **Purchase** your OUI-SPY board from [Tindie](https://www.tindie.com)
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

### Professional Audio System
- Multiple beep patterns for different alert types
- Variable frequency proximity indication
- Clean startup and ready signals
- Non-overlapping audio sequencing

---

**Choose your firmware above and start detecting!** 🚀

## License

Open source project. Hardware available commercially on Tindie. 
