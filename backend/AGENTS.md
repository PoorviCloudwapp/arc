# Backend Instructions

## Boundary
Backend owns APIs, business rules, authentication/authorization, integrations, jobs, and database access.

## Default structure
```text
backend/
└── src/
    ├── modules/
    │   └── <feature>/
    │       ├── <feature>.module.ts
    │       ├── <feature>.controller.ts
    │       ├── <feature>.service.ts
    │       ├── <feature>.repository.ts
    │       ├── dto/
    │       └── types/
    ├── common/
    ├── config/
    └── main.ts
```

Adapt names to the actual repository if an established structure differs.

## Responsibilities
- Controllers/routes: transport, validation, authentication guards, response mapping.
- Services: business logic and workflows.
- Repositories/data access: persistence operations.
- DTOs: request/response contracts.
- Modules: feature boundaries and dependency wiring.

## Rules
- Do not put business logic in controllers.
- Do not access the database directly from controllers.
- Reuse existing guards, pipes, middleware, exceptions, and utilities.
- Keep modules cohesive.
- Avoid circular dependencies.
- Do not change database schema without a migration when migrations are used.
