# ADR 0002 — Firestore vs SQL
Date: 2025-08-13
Status: Accepted

## Context
Mobile-first telemetry, hierarchical access, and near-real-time updates are key.

## Decision
Use Firestore (Native) as primary store. Re-evaluate if relational joins become dominant.

## Consequences
- Fast iteration and sync.
- Need defined indexes and careful data modelling.
