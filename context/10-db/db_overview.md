---
id: db.overview
title: Database Overview
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
related: [db.groups, db.boats, db.sensors, db.users_roles, db.alerts]
status: draft
---

Primary datastore: **Firestore (Native mode)**.
We model Groups (hierarchy), Boats (assigned to groups), Sensors (per boat), Users & Roles (RBAC), Alerts (rules & notifications).

### Naming conventions
- Collections: plural lower case (e.g., `groups`, `boats`).
- Document IDs: system-generated `grp_*`, `boat_*`, `sns_*`, `usr_*`.
