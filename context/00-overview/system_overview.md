---
id: overview.system
title: System Overview
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
related: [db.overview, api.overview, roles.permissions, alerts.overview, telemetry.overview]
status: draft
---

## Vision
Narrowboat Watch provides hierarchical monitoring of boats and sensors across marinas, basins, and jetties, with role-based access and remote alerts.

## High-level Architecture
```mermaid
flowchart LR
  subgraph Field
    Sensor1((Sensors)) -->|BLE/LoRa| Gateways
  end
  Gateways --> Ingest((Cloud Ingest))
  Ingest --> Firestore[(Firestore)]
  Firestore --> MobileApp[Mobile App]
  Firestore --> AdminPortal[Admin Portal]
  AdminPortal --> Alerting((Alert Engine))
  Alerting --> Email
  Alerting --> SMS
```
