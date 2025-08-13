# ADR 0001 — Record the Roles Model
Date: 2025-08-13
Status: Accepted

## Context
We require an RBAC model with hierarchical groups and boat-scoped Owner role.

## Decision
Adopt roles: SuperUser, GroupAdmin, Watchkeeper, Owner. Owners bind to boats. Group-scoped roles cascade to children.

## Consequences
- Simplifies permission checks.
- Clear responsibility split.
