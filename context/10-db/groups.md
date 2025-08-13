---
id: db.groups
title: Groups Collection
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

## Collection
**Path:** `/groups/{id}`

## Fields
- `name` (string, required) — Display name
- `parentId` (string|null) — Parent group or null for root
- `level` (integer) — 0–3 (derived from hierarchy)
- `groupType` (string) — marina|basin|jetty|custom
- `createdAt` (timestamp) — Server timestamp when created

## Indexes
- (parentId, name) composite
- (level) single

## Example
```json
{
  "name": "Marina A",
  "parentId": null,
  "level": 0,
  "groupType": "marina",
  "createdAt": "<serverTimestamp>"
}
```
