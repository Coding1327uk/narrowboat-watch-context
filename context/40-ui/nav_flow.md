---
id: ui.nav_flow
title: Navigation Flow
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

```mermaid
flowchart TD
  Login --> Dashboard -->|select boat| BoatDetail
  Dashboard --> AlertsList --> AlertDetail
  Dashboard --> GroupsTree --> GroupDetail
```
