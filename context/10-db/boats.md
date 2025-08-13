---
id: db.boats
title: Boats Collection
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

## Collection
**Path:** `/boats/{id}`

## Fields
- `name` (string, required) — Boat name
- `groupId` (string, required) — Assigned group ID
- `ownerIds` (array<string>) — User IDs with Owner role for this boat
- `lengthFt` (number) — Length in feet
- `notes` (string) — Free text
- `createdAt` (timestamp) — Server timestamp

## Indexes
- (groupId, name) composite

## Example
```json
{
  "name": "NB Willow",
  "groupId": "grp_123",
  "ownerIds": [
    "usr_9"
  ],
  "lengthFt": 57,
  "notes": "",
  "createdAt": "<serverTimestamp>"
}
```
