<div align="center">
<img width="124" height="124" alt="mirra-1024" src="https://github.com/user-attachments/assets/d8c9b04c-3839-444b-8522-fcb888c008dd" />

  # Mirra — Android Screen Mirror

  **Mirror your Android device on macOS, Windows, and Linux — no root required.**


[![Release](https://img.shields.io/github/v/release/sukushw/mirra-screen-mirror?label=latest&color=blue)](https://github.com/sukushw/mirra-screen-mirror/releases/latest)

[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey)](https://github.com/sukushw/mirra-screen-mirror/releases/latest)

---
</div>
## Overview

**Mirra** is a free, open-source desktop application that streams your Android screen to your computer in real time over USB or Wi-Fi — with zero lag and no ads. Built with Compose Multiplatform on top of the battle-tested [scrcpy](https://github.com/Genymobile/scrcpy) protocol.

> No root. No app install on Android. Just plug in and mirror.

---

## Screenshots

<!-- Main window -->

<img width="1203" height="779" alt="Screenshot 2026-04-13 at 10 58 52" src="https://github.com/user-attachments/assets/721ed9fb-c073-4ccd-bb83-6cd99fc50497" />



<!-- Live mirroring session -->
<img width="1204" height="782" alt="Screenshot 2026-04-13 at 10 59 28" src="https://github.com/user-attachments/assets/4e3ecf05-e52a-46b2-8c52-cb683f024050" />




---

## Features

- **USB Mirroring** — Connect your Android device via USB cable and start mirroring instantly
- **Wi-Fi Mirroring (Android 11+)** — Discover devices wirelessly on your local network via mDNS — no cable needed
- **Wi-Fi Mirroring (Android ≤ 10)** — Connect over TCP/IP after a one-time USB setup (`adb tcpip 5555`)
- **High Quality Streaming** — H.264 and H.265 codec support, up to 120 fps, up to native resolution
- **Low Latency** — FFmpeg-accelerated decoding optimized for live streaming
- **Clean UI** — Three-panel layout with device list, live viewport, and settings — built with Material Design 3
- **No Root Required** — Works with standard Android developer mode
- **Cross-Platform** — Runs natively on macOS (Apple Silicon & Intel), Windows, and Linux

---

## Download

### macOS

| Version | Chip | Download |
|---------|------|----------|
| 1.0.0   | Apple Silicon (M1/M2/M3/M4) | [Mirra-1.0.0-arm64.dmg](https://github.com/aniljsr52/mirra-screen-mirror/releases/download/v1.0.0/Mirra-1.0.0.dmg) |

> **Windows & Linux** packages coming soon.

---

## Requirements

| Requirement | Details |
|-------------|---------|
| Android version | 5.0 (Lollipop) or newer |
| USB debugging | Must be enabled in Developer Options |
| Computer OS | macOS 11+, Windows 10+, or Linux (x86_64) |
| Java | Bundled — no separate install needed |

---

## Setup Guide

### USB Connection (Fastest)

1. Enable **Developer Options** on your Android device:
   - Go to **Settings → About Phone**
   - Tap **Build Number** 7 times
2. Enable **USB Debugging** in **Settings → Developer Options**
3. Connect your device via USB cable
4. Open **Mirra** — your device will appear in the left panel
5. Click your device to start mirroring

### Wi-Fi Connection — Android 11+

1. Enable **Wireless Debugging** in **Settings → Developer Options**
2. Open **Mirra** — make sure your phone and computer are on the same Wi-Fi network
3. Your device will be discovered automatically — click to connect

### Wi-Fi Connection — Android 10 and below

1. Connect your device via USB first
2. Run the following in your terminal:
   ```sh
   adb tcpip 5555
   ```
3. Disconnect the USB cable
4. In **Mirra**, use **Direct TCP** and enter your device's IP address (find it in **Settings → About Phone → Status**)

---

## Settings

| Setting | Options | Default |
|---------|---------|---------|
| Max Frame Rate | 15, 30, 60, 90, 120 fps | 60 fps |
| Resolution | 720p, 1080p, 1440p, Native | 1080p |
| Video Codec | H.264, H.265 | H.264 |

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| UI Framework | [Compose Multiplatform](https://www.jetbrains.com/lk/compose-multiplatform/) (Material 3) |
| Language | Kotlin (JVM) |
| ADB Client | [dadb](https://github.com/mobile-dev-inc/dadb) |
| Video Decoding | [FFmpeg](https://ffmpeg.org/) via [JavaCPP](https://github.com/bytedeco/javacpp-presets) |
| Device Discovery | [JmDNS](https://github.com/jmdns/jmdns) (mDNS/Bonjour) |
| Mirror Protocol | [scrcpy](https://github.com/Genymobile/scrcpy) |
| Packaging | Gradle Compose Desktop Plugin |

---

## Troubleshooting

**Device not detected over USB**
- Make sure USB Debugging is enabled
- Try a different USB cable or port
- Run `adb devices` in your terminal to verify the device is recognized

**Black screen after connecting**
- Unlock your Android device (mirroring requires the screen to be on)
- Try reducing the resolution in Settings

**Wi-Fi device not appearing**
- Ensure both devices are on the same Wi-Fi network
- Check that Wireless Debugging is enabled (Android 11+)

---

## License

```
MIT License

Copyright (c) 2025 Kushwaha

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## Acknowledgements

- [Compose Multiplatform](https://github.com/JetBrains/compose-multiplatform) by JetBrains
- [scrcpy](https://github.com/Genymobile/scrcpy) by Genymobile — the open-source mirroring engine that powers Mirra
- [dadb](https://github.com/mobile-dev-inc/dadb) — pure Java ADB implementation

---

<div align="center">
  Made with ❤️ by aniljsr</a>
</div>
