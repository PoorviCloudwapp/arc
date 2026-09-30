# Frontend Instructions

## Boundary
Frontend owns presentation, client-side state, routing, forms, API consumption, and user interactions.

Framework-specific Cursor rules live in `.cursor/rules/`:
- React: `frontend-react.mdc`
- Angular: `frontend-angular.mdc`

## Default structure
```text
frontend/
└── src/
    ├── components/
    ├── pages/
    ├── hooks/          # React
    ├── services/
    ├── utils/
    ├── types/
    └── ...
```

For Angular, prefer `src/app/` with `core/`, `shared/`, and `features/<feature>/` when starting fresh. Adapt names to the actual repository if an established structure differs.

## Responsibilities
- Components: reusable presentation.
- Pages: route-level composition.
- Hooks (React) / feature services (Angular): reusable client behavior.
- Services: API communication and integration.
- Utils: pure reusable helpers.
- Types/models: shared frontend contracts.

## Rules
- Do not make API calls directly from presentational components.
- Reuse existing components before creating new ones.
- Avoid large components; extract cohesive pieces when needed.
- Keep business rules that must be trusted on the server.
- Handle loading, success, empty, and error states where relevant.
- Do not introduce a new state-management or networking pattern without justification.
