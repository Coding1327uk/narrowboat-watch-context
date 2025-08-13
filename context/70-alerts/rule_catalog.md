---
id: alerts.catalog
title: Rule Catalog
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

1. **Low Tank Level**
   - `lhs`: sensor.tank.percent
   - `op`: <=
   - `rhs`: 20
   - debounce: 10m

2. **High Bilge Water**
   - `lhs`: sensor.bilge.level
   - `op`: >=
   - `rhs`: 80
   - immediate

3. **Sensor Offline**
   - `lhs`: sensor.lastSeen
   - `op`: staleFor
   - `rhs`: PT6H
