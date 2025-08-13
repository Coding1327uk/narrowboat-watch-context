---
id: db.alerts
title: Alerts Collection
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

## Collection
**Path:** `/alerts/{id}`

## Fields
- `name` (string, required) — Rule name
- `scope` (object) — groupIds[] and/or boatIds[]
- `condition` (object) — Left operand, operator, right operand
- `channels` (array<string>) — email|sms|push
- `enabled` (boolean) — Is rule active?
- `createdBy` (string) — User ID
- `createdAt` (timestamp) — Server timestamp

## Indexes
- (enabled) single

## Example
```json
{
  "name": "Low Tank",
  "scope": {
    "boatIds": [
      "boat_1"
    ]
  },
  "condition": {
    "lhs": "sensor.tank.percent",
    "op": "<=",
    "rhs": 20
  },
  "channels": [
    "email"
  ],
  "enabled": true,
  "createdBy": "usr_1",
  "createdAt": "<serverTimestamp>"
}
```
