# Frontend Instructions

## Boundary
Frontend owns presentation, client-side state, routing, forms, API consumption, and user interactions.

## Default structure
```text
frontend/
└── src/
    ├── components/
    ├── pages/
    ├── hooks/
    ├── services/
    ├── utils/
    ├── types/
    └── ...
```

Adapt names to the actual repository if an established structure differs.

## Responsibilities
- Components: reusable presentation.
- Pages: route-level composition.
- Hooks: reusable stateful behavior.
- Services: API communication and integration.
- Utils: pure reusable helpers.
- Types: shared frontend contracts.

## Rules
- Do not make API calls directly from presentational components.
- Reuse existing components before creating new ones.
- Avoid large components; extract cohesive pieces when needed.
- Keep business rules that must be trusted on the server.
- Handle loading, success, empty, and error states where relevant.
