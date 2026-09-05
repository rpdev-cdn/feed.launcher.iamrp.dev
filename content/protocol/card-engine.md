---
title: "Card Rendering Engine"
description: "Jetpack Compose card rendering architecture, JSON card schemas, and dynamic theming."
---

# Card Rendering Engine

RPDev Feed's UI layer is written entirely in **Jetpack Compose**, delivering declarative, reactive, 120Hz smooth scrolling across all screen sizes.

---

## 1. Card Hierarchy & Templates

Every card rendered in the feed implements the `FeedCard` component interface:

```kotlin
@Composable
fun FeedCardContainer(
    title: String,
    iconRes: Int?,
    actions: @Composable () -> Unit = {},
    content: @Composable () -> Unit
) {
    Card(
        modifier = Modifier
            .fillMaxWidth()
            .padding(horizontal = 16.dp, vertical = 8.dp),
        shape = RoundedCornerShape(24.dp),
        colors = CardDefaults.cardColors(
            containerColor = MaterialTheme.colorScheme.surfaceVariant
        )
    ) {
        Column(modifier = Modifier.padding(16.dp)) {
            FeedCardHeader(title, iconRes, actions)
            Spacer(modifier = Modifier.height(12.dp))
            content()
        }
    }
}
```

---

## 2. Card JSON Schema (v1)

External modules provide card payloads adhering to the official JSON schema:

```json
{
  "schema": "https://cdn.iamrp.dev/feed/schemas/card-v1.schema.json",
  "cardId": "hw_telemetry_01",
  "moduleId": "plugin_sensors",
  "title": "Hardware Health",
  "timestamp": 1788639000,
  "layout": "grid_metric",
  "items": [
    { "label": "Battery Temp", "value": "29.4 °C", "status": "nominal" },
    { "label": "CPU Load", "value": "14 %", "status": "nominal" },
    { "label": "RAM Free", "value": "4.2 GB", "status": "good" }
  ]
}
```

Full schema specification available at: [cdn.iamrp.dev/feed/schemas/card-v1.schema.json](https://cdn.iamrp.dev/feed/schemas/card-v1.schema.json).
