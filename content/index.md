---
title: "RPDev Feed"
description: "Sovereign, privacy-first minus-one screen feed engine elevating traditional RSS into a dynamic, rich mobile dashboard."
---

# 🌟 RPDev Feed

> **The Spotlight of the Show: Transforming Basic RSS into an Intelligent, Privacy-Respecting Minus-One Dashboard.**

```
  ███████╗███████╗███████╗██████╗     ███████╗███████╗███████╗██████╗ 
  ██╔════╝██╔════╝██╔════╝██╔══██╗    ██╔════╝██╔════╝██╔════╝██╔══██╗
  █████╗  █████╗  █████╗  ██║  ██║    █████╗  █████╗  █████╗  ██║  ██║
  ██╔══╝  ██╔══╝  ██╔══╝  ██║  ██║    ██╔══╝  ██╔══╝  ██╔══╝  ██║  ██║
  ██║     ███████╗███████╗██████╔╝    ██║     ███████╗███████╗██████╔╝
  ╚═╝     ╚══════╝╚══════╝╚═════╝     ╚═╝     ╚══════╝╚══════╝╚═════╝ 
```

---

## 🎯 The Star of the Show: Beyond Flat RSS

For decades, RSS has been the gold standard of open web syndication. But traditional RSS readers force you into flat, chronological list views disconnected from the rest of your digital life. Meanwhile, commercial launcher feeds like Google Discover invade your privacy with intrusive behavioral profiling, clickbait headlines, and sponsored tracking pixels.

**RPDev Feed bridges these worlds.** It delivers the rich, dynamic visual experience of a modern intelligent stream while upholding total user sovereignty and zero-tracking privacy:

- 📰 **RSS Reimagined**: Ingests raw RSS/Atom feeds with on-device HTML parsing, distraction-free reading, and smart headline summarization.
- ⚡ **Dynamic Context Cards**: Seamlessly blends RSS feeds with real-time on-device context: **[Privacy Weather](https://launcher.repo.iamrp.dev/catalog/modules/weather)**, **[Hardware Diagnostics](https://launcher.repo.iamrp.dev/catalog/modules/sensors)**, and **[Calendar Agendas](https://launcher.repo.iamrp.dev/catalog/modules/calendar)**.
- 🧩 **Extensible Module Ecosystem**: Query, install, reorder, and configure community modules from the **[RPDev Repository](https://launcher.repo.iamrp.dev)** directly inside the feed UI.
- 🔒 **Sovereign & On-Device**: Zero intermediate proxy servers. All feed URLs, weather endpoints, and IoT requests are fetched directly from your mobile device.

---

## 📱 Visual Showcase: DevPixel16 (Android 16)

| -1 Screen Overlay & Radar | Live Article Stream | Main Hub Telemetry |
|:---:|:---:|:---:|
| <img src="/static/images/feed_overlay_devpixel16.png" width="260" alt="-1 Screen Overlay"/> | <img src="/static/images/feed_overlay_articles_devpixel16.png" width="260" alt="Articles Stream"/> | <img src="/static/images/feed_main_devpixel16.png" width="260" alt="Main Hub Telemetry"/> |

| In-App Module Catalog | Active Plugin Manager | Data Sources & Settings |
|:---:|:---:|:---:|
| <img src="/static/images/feed_catalog_devpixel16.png" width="260" alt="In-App Module Catalog"/> | <img src="/static/images/feed_plugins_devpixel16.png" width="260" alt="Plugin Manager"/> | <img src="/static/images/feed_datasources_devpixel16.png" width="260" alt="Data Sources"/> |

---

## 🚀 Core Architectural Highlights

1. **Universal AIDL Overlay Bridge**: Interfaces over Android's `com.android.launcher3.WINDOW_OVERLAY` AIDL contract. Works seamlessly with **[RPDev Launcher](https://launcher.iamrp.dev)**, Nova Launcher, Lawnchair, and any launcher supporting the Google Overlay protocol.
2. **High-Performance Jetpack Compose UI**: Silky smooth 120Hz scrolling, predictive drag-to-dismiss animations, and Material You dynamic color harmonizing.
3. **Dynamic In-App Store**: Browse and install modules live from `launcher.repo.iamrp.dev` without sideloading or rebuilding the app.

---

## 🧭 Documentation Index

| Section | Topic | Link |
|---|---|---|
| 🌟 **The RSS Evolution** | How RPDev Feed transforms RSS into a modern dynamic stream | [RSS Evolution](spotlight/rss-evolution.md) |
| 🔌 **Overlay Protocol** | AIDL interface, IPC handshake, and window attachment mechanics | [Overlay Bridge](protocol/overlay-bridge.md) |
| 🎴 **Card Engine** | HubCardData composite models, chip tags, and timeline layouts | [Card Engine](protocol/card-engine.md) |
| 🧩 **Module Architecture** | Dynamic registration, SharedPreferences configs, and lifecycle | [Module System](plugins/module-system.md) |
| 🛠️ **Developer Tutorial** | Step-by-step guide to writing your own HubPlugin | [Developer Guide](plugins/developer-guide.md) |
| 🛡️ **Privacy Guarantees** | Audit of network isolation, local storage, and zero telemetry | [Privacy Audit](settings/telemetry-privacy.md) |
| 📥 **Download APK** | Official signed builds of RPDev Feed (v1.2.1 GA) | [Download v1.2.1](download.md) |

---

## 🌐 Connected Ecosystem

- **RPDev Launcher**: [launcher.iamrp.dev](https://launcher.iamrp.dev)
- **Module Repository**: [launcher.repo.iamrp.dev](https://launcher.repo.iamrp.dev)
- **Edge CDN & Manifests**: [cdn.iamrp.dev](https://cdn.iamrp.dev)
