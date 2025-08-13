---
id: telemetry.overview
title: Telemetry Overview
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

We repurpose acceleration fields (X, Y, Z) in RuuviTag-like packets as custom fields `Data1, Data2, Data3` per sensor type. Server-side decoding maps by `sensors.type`.

**Common envelope**
```json
{
  "mac": "AA:BB:CC:DD:EE:FF",
  "ts": "2025-08-12T12:34:56Z",
  "rssi": -70,
  "payload": {"Data1": 42, "Data2": 10, "Data3": 3}
}
```
