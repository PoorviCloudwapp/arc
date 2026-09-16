# System Architecture

## Applications
- Backend: `backend/`
- Frontend: `frontend/`
- Mobile: `mobile/`

Replace or extend these according to the actual repository.

## High-level flow
```text
Client
  -> API
  -> Application/Business Logic
  -> Data Access
  -> Database
```

## Architecture principles
1. Keep business logic inside clear feature boundaries.
2. Keep transport, business logic, and persistence concerns separated.
3. Prefer existing patterns.
4. Keep dependencies flowing toward stable abstractions.
5. Make architectural decisions explicit through ADRs.

## Source of truth
The actual code and database schema are authoritative for implementation details.
This document describes intended boundaries, not every file.
