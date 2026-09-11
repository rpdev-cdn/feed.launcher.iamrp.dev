---
title: "Feed Module System & Lifecycle"
description: "How RPDev Feed loads modules dynamically, validates signatures, and manages lifecycle."
---

# Feed Module System & Lifecycle

RPDev Feed separates the feed presentation container from informational content using a modular plugin architecture.

---

## 1. HubPluginRegistry

The core coordinator is `HubPluginRegistry.kt`:

- Scans installed APK packages advertising the module intent: `iamrp.dev.feed.MODULE`.
- Loads dynamic module definitions and instantiates card generators.
- Manages background refresh intervals to avoid battery drain.
- Dispatches user actions (clicks, button taps) back to host modules.

---

## 2. HubModuleManager & Catalog Sync

`HubModuleManager.kt` synchronizes available modules against the sovereign catalog:

1. Queries primary catalog endpoint: `https://launcher.repo.iamrp.dev/catalog/modules.json`.
2. Fallback secondary CDN endpoint: `https://cdn.iamrp.dev/feed/modules.json`.
3. Fallback tertiary Git mirror: `https://raw.githubusercontent.com/RPDevs-Builds/RPDev-Feed-Modules/main/catalog/modules.json`.
4. Caches catalog responses locally in SharedPreferences to ensure instant offline launching.

Users can enable, disable, configure, or uninstall modules directly from the Feed Settings menu.
