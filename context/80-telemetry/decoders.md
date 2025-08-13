---
id: telemetry.decoders
title: Telemetry Decoders
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

| type   | Data1     | Data2     | Data3     | Derived |
|--------|-----------|-----------|-----------|---------|
| tank   | percent   | tempC     | voltageV  | status=OK/WARN/CRIT |
| temp   | tempC     | humidity% | reserved  | comfortIdx |
| door   | state(0/1)| batteryV  | reserved  | openTime |
| volt   | volts     | reserved  | reserved  | lowVoltage? |
