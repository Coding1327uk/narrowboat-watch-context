---
id: alerts.overview
title: Alert Engine Overview
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

Alert rules evaluate telemetry/state against conditions and dispatch via channels.

**Condition model**
- `lhs`: data path (e.g., `sensor.tank.percent`)
- `op`: one of `<, <=, ==, >=, >, !=, crossesBelow, crossesAbove, staleFor`
- `rhs`: number/string or duration (e.g., `PT2H` for 2 hours)

**Channels**: email, sms, push
