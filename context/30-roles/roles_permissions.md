---
id: roles.permissions
title: Roles & Permissions
version: 0.2.0
owners: [simon]
last_updated: 2025-08-13
status: draft
---

| Role        | Scope reference | Can View | Can Manage | Notes |
|-------------|------------------|----------|------------|-------|
| SuperUser   | all groups       | ✅        | ✅          | Platform-level ops |
| GroupAdmin  | groupIds[]       | ✅        | ✅ (in scope) | Cascades into child groups |
| Watchkeeper | groupIds[]       | ✅        | ❌          | Monitor-only |
| Owner       | boatIds[]        | ✅ (their boats) | ❌ | Bound to boats |

**Access Cascade:** Assigning `GroupAdmin` or `Watchkeeper` on a parent group implicitly grants access to all descendant groups.
