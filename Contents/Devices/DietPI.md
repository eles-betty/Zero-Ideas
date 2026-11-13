# Raspberry Pi 3B+ Project

## About this Repo

I have Raspberry Pi 3B+ which is old enough and has limited hardware to keep up with modern OSs, so I think it's useful to install lightweight OSs. Besides, I don't have a monitor and am not planning (yet) to use GPIO pins, so I consider making this Raspberry a server and installing apps that use SSH (no desktop environment / headless mode).

So I checked Reddit, XDA, and some online posts and found that Raspberry Pi OS (minimal / no DEs) and DietPi are easier to install and work perfectly fine on this old hardware. I can free up more RAM, so I prefer DietPi minimal too, which gives me some extra MBs of RAM and significant performance improvements considering its limited hardware.

### Hardware Specification

[skip to Disclaimer](#disclaimer) or [skip to Installing Diet Pi](#installing-diet-pi-os)

**Here is Tehcnical Specification of Raspberry Pi 3B + :**

- Processor: Broadcom BCM2837B0, Cortex-A53 64-bit Quads-Core SoC @ 1.4 GHz
- Memory: 1 GB LPDDR2 SDRAM
- Wireless Connectivity: Dual-band 2.4 GHz and 5 GHz IEEE 802.11 b/g/n/ac Wi-Fi, Bluetooth 4.2 / BLE  
- Wired Networking: Gigabit Ethernet over USB 2.0 (maximum throughput capped at 300 Mbps)
- Power Over Ethernet: PoE support (requires an optional separate PoE HAT)  
- GPIO: Extended 40-pin GPIO header
- Video & Audio Output: Full-size HDMI port, MIPI DSI display port, MIPI CSI camera port, and a 4-pole 3.5mm stereo/composite video jack
- USB Ports: 4 × USB 2.0 ports  
- Storage: MicroSD card slot for operating system installation and local storage
- Power Requirements: 5V / 2.5A DC via Micro-USB port or GPIO header

### OSs Specification

[skip to Disclaimer](#disclaimer)

**Here is Rasperry OS Lite VS DietPi OS Performance on Raspberry Pi 3B+ :**

| Metric / Aspect | Raspberry Pi OS (Lite / Headless) | DietPi (Headless) | Impact on Raspberry Pi 3B+ |
| :--- | :--- | :--- | :--- |
| **Idle RAM Usage** | ~80 MB – 150 MB | **~30 MB – 50 MB** | DietPi saves ~50–100 MB of RAM, freeing up vital headroom on the 1 GB total RAM limit. |
| **Storage Footprint (Fresh Install)** | ~1.5 GB – 2.0 GB | **~600 MB – 800 MB** | DietPi uses fewer SD card blocks, leading to faster initial backups and less SD wear. |
| **Active Processes at Boot** | ~30 – 45 processes | **~15 – 20 processes** | Fewer background daemons mean lower CPU overhead and less background polling. |
| **Boot Time (to Shell)** | ~18 – 25 seconds | **~10 – 15 seconds** | DietPi initializes faster due to stripped-down startup scripts and minimal services. |
| **RAM Logging (Log2Ram)** | Optional (requires manual setup) | **Built-in by default** | DietPi writes logs to RAM instead of the SD card, improving write speeds and extending SD card lifespan. |
| **CPU Governor / Throttling** | `ondemand` (default balanced) | `ondemand` (easily tweakable via `dietpi-config`) | DietPi allows easy one-click CPU governor adjustments (e.g., `performance`, `powersave`). |
| **Software Management Overhead** | Standard `apt` package manager | Custom `dietpi-software` wrapper over `apt` | `dietpi-software` installs pre-configured, optimized software builds that consume less RAM/CPU. |

## Disclaimer

- Good SD Card : Minimum Class 10 or A1 at 16GB of storage
- Other Connected Devices :
  - Printer : HP Smart Tank 520
  - Modem : ZTE F609
- Read carefully, do it at your own risk !!! I don't resoponsible of any data loss or hardware malfuncion

## Installing Diet Pi OS

- On MacOS (link to MacOS_Tahoe.md) / Windows (link to Windows_10-11.md) / Linux (link to LinuxMint.md), install the `Raspberry Pi Imager` (recommended by Raspberry Pi).
- Insert SD Card on the Card Reader, and connect to your PC / Laptop, wait less than a minute so your OS detect the SD Card, accept permission (if its first time connected) and after that open the `Raspberry Pi Imager` app.
-

## Installing Applications

### Scenario for the Project

Based on my need, i will do some project for testing like:

- Print Server
- Lightweight Web Server
- Docker Based App

### Apps & Configuration
