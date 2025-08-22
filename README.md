# OUI-SPY - Detector

![OUI-SPY](ouispy.png)

Professional BLE scanning system that detects specific devices by MAC address or OUI with audio feedback.

## Hardware

**OUI-SPY Board** - Available on [Tindie](https://www.tindie.com)
- ESP32-S3 based detection system
- Integrated buzzer and power management
- Ready-to-use, no additional components required

**Alternative:** Standard ESP32-S3 with external buzzer on GPIO3

## Available Firmwares

### 1. OUI-SPY (Original)
**Professional BLE scanning system for device detection**
- OUI filtering for device manufacturers
- Full MAC address matching
- Persistent configuration storage
- Audio feedback system
- Privacy-focused with MAC randomization

### 2. Flock You - Surveillance Camera Detection
**Advanced detection system for Flock Safety cameras and surveillance devices**

[![Flock You](https://github.com/colonelpanichacks/flock-you/raw/main/flock.png)](https://github.com/colonelpanichacks/flock-you)

**Features:**
- **Multi-Method Detection**: WiFi promiscuous mode + BLE scanning
- **Surveillance Device Detection**: Flock Safety, Penguin, Pigvision systems
- **Real-time Audio Alerts**: Boot sequence, detection alerts, heartbeat monitoring
- **Comprehensive JSON Output**: Detailed device information and threat assessment
- **Channel Hopping**: Automatic WiFi channel cycling (1-13)
- **Pattern Recognition**: SSID, MAC prefix, and device name matching

**Detection Coverage:**
- WiFi probe requests and beacon frames
- BLE advertisement scanning
- Known surveillance device signatures
- MAC address filtering with real-world databases

**Audio Alert System:**
- Boot sequence: 2 beeps (low → high pitch)
- Detection alert: 3 fast high-pitch beeps
- Heartbeat pulse: 2 beeps every 10 seconds while device in range
- Range monitoring with departure detection

**Source Code:** [Flock You Repository](https://github.com/colonelpanichacks/flock-you)

## Quick Start

1. **Power on device** - Creates WiFi AP `snoopuntothem` (password: `astheysnoopuntous`)
2. **Connect and configure** - Navigate to `http://192.168.4.1`
3. **Add targets** - Enter OUI prefixes (`AA:BB:CC`) or full MAC addresses
4. **Save configuration** - Device automatically switches to scanning mode

## Features

### Detection System
- OUI filtering for device manufacturers
- Full MAC address matching
- Persistent configuration storage
- Automatic timeout handling

### Audio Feedback
- 2 ascending beeps: Ready to scan
- 3 beeps: New device detected
- 2 beeps: Known device re-detected (5+ seconds)
- Smart cooldown prevents spam

### Privacy
- MAC address randomization on boot
- Stealth mode operation
- No traceable hardware fingerprints

## Installation

### PlatformIO
```bash
cd ouibuzzer-main/ouibuzzer
python3 -m platformio run --target upload
```

### Dependencies
- NimBLE-Arduino ^1.4.0
- ESP Async WebServer ^3.0.6
- Preferences ^2.0.0

## Configuration

### Web Portal
Access via `http://192.168.4.1` after connecting to `snoopuntothem` AP:

**OUI Prefixes:** `AA:BB:CC` (matches specific manufacturers)
**MAC Addresses:** `AA:BB:CC:12:34:56` (specific devices)

Multiple entries supported (one per line).

### Filter Types
- **OUI:** First 3 bytes (manufacturer prefix)
- **MAC:** Complete 6-byte address
- **Format:** Supports colons, hyphens, or spaces

## Operation

### Startup Sequence
1. MAC randomization (stealth mode)
2. Configuration mode (20-second timeout)
3. BLE scanning activation
4. Target detection and audio alerts

### Detection Logic
- Continuous BLE scanning
- Real-time MAC/OUI matching
- Cooldown system prevents duplicate alerts
- Memory management for device tracking

## Serial Output

```
=== OUI Spy Enhanced BLE Detector ===
Original MAC: d8:3b:da:45:aa:a0
Randomized MAC: a2:f3:91:7e:8c:45

=== STARTING SCANNING MODE ===
Configured Filters:
- AA:BB:CC (OUI)
- AA:BB:CC:12:34:56 (MAC)

>> Match found! <<
Device: AA:BB:CC:ab:cd:ef | RSSI: -45
Filter matched: OUI
```

## Troubleshooting

**No WiFi AP:** Wait 30 seconds after power-on
**No web portal:** Ensure connected to `snoopuntothem`, disable mobile data
**No audio:** Check buzzer connection (GPIO3)
**No detection:** Verify target device is advertising BLE

## Technical Specifications

- **Platform:** ESP32-S3
- **Scan interval:** 3 seconds
- **Range:** 10-30 meters (typical)
- **Storage:** NVS flash memory
- **Processing:** Dual-core optimization

## License

Open source project. Modifications welcome. 
