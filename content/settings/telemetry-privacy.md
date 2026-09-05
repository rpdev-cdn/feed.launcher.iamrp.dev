---
title: "Privacy & Zero Telemetry Architecture"
description: "Why RPDev Feed is completely private, local-first, and free from third-party tracking."
---

# Privacy & Zero Telemetry Architecture

Unlike proprietary feed engines (Google Discover, Microsoft Start, Samsung Free), RPDev Feed is designed from the ground up for total privacy sovereignty.

---

## 1. Zero Tracking Guarantees

| Feature | Google Discover | RPDev Feed |
|---|---|---|
| Behavioral Ad Profiling | Yes (mandatory) | ❌ **None** |
| Location Tracking | Continuous background polling | ❌ **None** (Manual city or device GPS only if weather module enabled) |
| Reading Habits Recorded | Synced to Google Account | ❌ **Stored only in local SQLite cache** |
| Ad Network SDKs | AdMob, DoubleClick | ❌ **Zero ad SDKs** |
| Cloudflare DNS Privacy | Custom DNS ignored | ✅ **Direct DoH over Cloudflare 1.1.1.1** |

---

## 2. On-Device Storage Model

All feed data, module states, and cached card layouts are stored in app-private SQLite databases and SharedPreferences:

- File: `/data/data/iamrp.dev.feed/databases/feed_cache.db`
- File: `/data/data/iamrp.dev.feed/shared_prefs/hub_module_manager_prefs.xml`

Uninstalling or clearing app data wipes 100% of stored records instantly.
