# Cursor Agentic Coding Framework

This framework is designed for Cursor Agent with low context overhead and systematic development.

## Install

Copy these files/folders into the root of an existing project:

- `AGENTS.md`
- `.cursor/rules/`
- `.cursor/skills/`
- `specs/`
- `backend/AGENTS.md`
- `frontend/AGENTS.md`
- `mobile/AGENTS.md`

Do not replace existing application source code.

## First customization

1. Edit `AGENTS.md` only for project-wide rules.
2. Edit `.cursor/rules/02-architecture.mdc` for your high-level boundaries.
3. Replace the placeholder `specs/product.md`.
4. Replace `specs/architecture.md` with your actual architecture.
5. Customize `backend/AGENTS.md`, `frontend/AGENTS.md`, and `mobile/AGENTS.md`.
6. Keep feature specs small and focused.

## Recommended workflow

Small change:
Request -> inspect relevant files -> implement -> verify.

Feature:
Request -> requirements -> design -> tasks -> implement -> verify -> update tasks/spec.

Architecture change:
Problem -> ADR -> design -> implementation -> verification.

## Token-efficiency principles

- Keep always-applied rules short.
- Use directory-specific AGENTS.md for local context.
- Load feature specs only when the feature is being worked on.
- Prefer references to canonical documents over copying documentation into rules.
- Never instruct the agent to read the entire repository by default.
- Search for existing patterns before creating new ones.

## Important

This is a framework/template, not a requirement to use the example folder names. Your existing backend/frontend structure remains authoritative after you document it in the appropriate AGENTS.md and architecture files.
