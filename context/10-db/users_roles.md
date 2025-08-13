---
id: db.users_roles
title: Users & Roles
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

## Collection
**Path:** `/users/{id}`

## Fields
- `displayName` (string) — User friendly name
- `email` (string) — Used for login/notifications
- `roles` (array<object>) — Each: roleType + groupIds[] or boatIds[]
- `createdAt` (timestamp) — Server timestamp

## Indexes
- (email) unique

## Example
```json
{
  "displayName": "Alex",
  "email": "alex@example.com",
  "roles": [
    {
      "roleType": "GroupAdmin",
      "groupIds": [
        "grp_1",
        "grp_2"
      ]
    },
    {
      "roleType": "Owner",
      "boatIds": [
        "boat_1"
      ]
    }
  ],
  "createdAt": "<serverTimestamp>"
}
```
