---
title: "Overlay Bridge AIDL Protocol"
description: "Detailed specification of the Android Launcher Overlay AIDL interface, ClientService handshake, and window attachment."
---

# Overlay Bridge AIDL Protocol

RPDev Feed implements the standard `ILauncherOverlay` and `ILauncherOverlayCallback` AIDL specifications, allowing any compatible Android launcher to host the feed as a seamless horizontal drawer.

---

## 1. AIDL Interface Definition

Communication occurs over Android IPC via bound services:

```
┌────────────────────────┐                   ┌────────────────────────┐
│     RPDev Launcher     │   Binder IPC      │       RPDev Feed       │
│  (com.android.launcher)│ ────────────────> │    (iamrp.dev.feed)    │
│                        │ <──────────────── │                        │
│ ILauncherOverlayCallback│                   │    ILauncherOverlay    │
└────────────────────────┘                   └────────────────────────┘
```

### Key Methods:
- `openOverlay(int options)`: Triggers open animation from launcher tap or swipe.
- `closeOverlay(int options)`: Dismisses the feed back to the home screen.
- `onScroll(float progress)`: Real-time dragging feedback (`0.0f` = fully closed, `1.0f` = fully opened).
- `windowAttached(WindowManager.LayoutParams lp, ILauncherOverlayCallback cb, int flags)`: Transmits window token and display configuration.

---

## 2. Intent Filter Registration

In `AndroidManifest.xml`, RPDev Feed registers its service:

```xml
<service
    android:name=".service.OverlayService"
    android:exported="true"
    android:permission="com.google.android.launcher.permission.OVERLAY">
    <intent-filter>
        <action android:name="com.android.launcher3.WINDOW_OVERLAY" />
        <category android:name="android.intent.category.DEFAULT" />
    </intent-filter>
</service>
```

Launchers query for services handling `com.android.launcher3.WINDOW_OVERLAY` to automatically discover RPDev Feed.
