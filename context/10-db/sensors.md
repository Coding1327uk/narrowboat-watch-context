---
id: db.sensors
title: Sensors Collection
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

## Collection
**Path:** `/sensors/{id}`

## Fields
- `mac` (string, required) — Unique MAC or EUI
- `name` (string) — Human label
- `type` (string, required) — tank|temp|door|voltage|custom
- `boatId` (string) — Associated boat
- `dataFields` (object) — Custom-encoded fields Data1–Data3
- `lastSeen` (timestamp) — Last telemetry time
- `createdAt` (timestamp) — Server timestamp

## Indexes
- (boatId, type) composite
- (mac) unique

## Example
```json
{
  "mac": "AA:BB:CC:DD:EE:FF",
  "name": "Tank 1",
  "type": "tank",
  "boatId": "boat_1",
  "dataFields": {
    "Data1": 42,
    "Data2": 10,
    "Data3": 3
  },
  "lastSeen": "2025-08-01T12:00:00Z",
  "createdAt": "<serverTimestamp>"
}
```
