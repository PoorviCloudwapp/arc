# Mobile Instructions

## Boundary
Mobile owns mobile UI, navigation, local state, device capabilities, and API consumption.

Follow MVC inside the `mobile/` folder. Prefer the project's actual framework and this layout unless an established structure already differs.

## Default structure
```text
mobile/
├── models/          # data shapes, local entities, mappers
├── views/           # screens, widgets, UI only
├── controllers/     # UI orchestration, input handling, navigation triggers
├── services/        # API / device / storage access
├── navigation/      # routes and navigators (if present)
└── utils/           # pure helpers
```

## Responsibilities
- Models: data structures, parsing/mapping, local persistence shapes. No UI.
- Views: presentation and user interaction only. No API calls.
- Controllers: wire views to models/services; loading/error flow and navigation intents.
- Services: HTTP, device APIs, secure storage — network access lives here.

## Rules
- Reuse existing widgets/components and services.
- Keep API calls in the service/API layer; never call the network from views.
- Do not duplicate backend business rules.
- Handle offline, loading, empty, success, and error states where applicable.
- Do not introduce a new state-management or networking pattern without justification.
- Keep controllers thin: orchestrate, do not become a second backend.
