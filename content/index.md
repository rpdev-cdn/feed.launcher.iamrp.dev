---
title: "RPDev Feed"
description: "Sovereign, privacy-first, extensible feed provider for Android home screens and third-party launchers."
---

# RPDev Feed

> An open-source, modular, and privacy-respecting Google Discover alternative built on Jetpack Compose and the Android Launcher Overlay AIDL protocol.

```
  ███████╗███████╗███████╗██████╗     ███████╗███████╗███████╗██████╗ 
  ██╔════╝██╔════╝██╔════╝██╔══██╗    ██╔════╝██╔════╝██╔════╝██╔══██╗
  █████╗  █████╗  █████╗  ██║  ██║    █████╗  █████╗  █████╗  ██║  ██║
  ██╔══╝  ██╔══╝  ██╔══╝  ██║  ██║    ██╔══╝  ██╔══╝  ██╔══╝  ██║  ██║
  ██║     ███████╗███████╗██████╔╝    ██║     ███████╗███████╗██████╔╝
  ╚═╝     ╚══════╝╚══════╝╚═════╝     ╚═╝     ╚══════╝╚══════╝╚═════╝ 
```

---

## What is RPDev Feed?

RPDev Feed attaches directly to the **-1 (minus-one) screen** of your launcher, providing dynamic informational cards, device telemetry, weather radar, and customizable widgets without commercial ads, clickbait, or behavioral profiling.

### Key Pillars:
- 📱 **Universal Launcher Compatibility**: Works with **[RPDev Launcher](https://launcher.iamrp.dev)**, Nova Launcher, Lawnchair, and any launcher implementing the standard Google Overlay protocol (`com.android.launcher3.WINDOW_OVERLAY`).
- 🧩 **Modular Plugin Ecosystem**: Extend your feed with swappable modules from the **[RPDev Repository](https://repo.launcher.iamrp.dev)**.
- 🎨 **Modern Jetpack Compose UI**: Silky smooth 120Hz card rendering, Material You dynamic color harmonizing, and dark mode parity.
- 🔒 **Absolute Privacy**: Zero telemetry, zero ad tracking. All sensor readings and RSS data are fetched directly by your device.

---

## Documentation Index

| Guide | Description | Link |
|---|---|---|
| **Overlay Bridge Protocol** | AIDL architecture, IPC handshake, and window attachment | [Overlay Bridge](protocol/overlay-bridge.md) |
| **Card Rendering Engine** | Compose UI card hierarchy and JSON schema v1 | [Card Engine](protocol/card-engine.md) |
| **Module Architecture** | Dynamic DEX loading and HubPluginRegistry | [Module System](plugins/module-system.md) |
| **Developer Tutorial** | Build your first custom feed card module | [Developer Guide](plugins/developer-guide.md) |
| **Privacy Architecture** | Zero tracking guarantees and local storage | [Privacy & Telemetry](settings/telemetry-privacy.md) |
| **Downloads** | Download official APK releases | [Download APK](download.md) |

---

## Ecosystem Services

- **RPDev Launcher**: [launcher.iamrp.dev](https://launcher.iamrp.dev)
- **RPDev Feed Portal**: [feed.launcher.iamrp.dev](https://feed.launcher.iamrp.dev)
- **Module Repository**: [repo.launcher.iamrp.dev](https://repo.launcher.iamrp.dev)
- **Edge Delivery CDN**: [cdn.iamrp.dev](https://cdn.iamrp.dev)
