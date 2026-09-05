---
title: "Developer Guide: Creating a Feed Module"
description: "Step-by-step tutorial on building a custom Feed Module for RPDev Feed."
---

# Developer Guide: Creating a Feed Module

Learn how to build and publish a custom Feed Module that displays dynamic cards inside RPDev Feed.

---

## 1. Project Structure

A feed module can be built as a standalone Android application or library:

```
my-feed-module/
├── AndroidManifest.xml
├── build.gradle.kts
└── src/main/java/com/example/mymodule/
    ├── MyCardProvider.kt
    └── MyModuleService.kt
```

---

## 2. Declare Module Intent in Manifest

In your `AndroidManifest.xml`, declare your service with the `iamrp.dev.feed.MODULE` action:

```xml
<service
    android:name=".MyModuleService"
    android:exported="true">
    <intent-filter>
        <action android:name="iamrp.dev.feed.MODULE" />
    </intent-filter>
    <meta-data
        android:name="iamrp.dev.feed.MODULE_METADATA"
        android:resource="@xml/module_manifest" />
</service>
```

---

## 3. Define the Module Manifest (`res/xml/module_manifest.xml`)

```xml
<?xml version="1.0" encoding="utf-8"?>
<module
    id="plugin_sample"
    name="Sample Stock Ticker"
    version="1.0.0"
    author="YourName"
    category="Finance"
    summary="Live stock and crypto tickers on your feed" />
```

---

## 4. Submitting to Repository

Once built and tested on emulator or device, submit your module PR to the **[RPDev Feed Modules Repository](https://repo.launcher.iamrp.dev)** for inclusion in the master catalog.
