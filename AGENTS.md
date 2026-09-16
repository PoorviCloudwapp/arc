# Project Instructions

## Purpose
This repository uses a lightweight, spec-driven workflow optimized for Cursor Agent.
Keep context small, changes focused, and architecture consistent.

## Before coding
1. Understand the request and classify it as small, feature, bug, refactor, or architectural.
2. Identify the affected application/module.
3. Read applicable `AGENTS.md` files from the repository root down to the target directory.
4. Read only the relevant specification under `specs/`.
5. Inspect existing implementation patterns before creating new abstractions.
6. For non-trivial work, create or update the feature task list before implementation.

## Coding
- Follow repository architecture and existing patterns.
- Reuse existing utilities, services, components, and abstractions.
- Do not duplicate business logic.
- Do not modify unrelated files.
- Do not introduce dependencies unless necessary.
- Do not silently change public API contracts or database behavior.
- Do not invent requirements.

## Context discipline
- Do not read the entire repository unless explicitly required.
- Load only files relevant to the current task.
- Prefer indexes, module documentation, and feature specs before broad source exploration.
- When a canonical document exists, reference it instead of duplicating its content into rules.

## Verification
After implementation, run the smallest relevant verification:
- tests
- type checking
- linting
- build, when relevant

Report changed files, verification performed, and any remaining uncertainty.

## Completion
For non-trivial changes:
- update the feature task checklist
- update relevant specifications if behavior changed
- add an ADR only when a durable architectural decision was made
