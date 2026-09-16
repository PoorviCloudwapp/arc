# Specifications

Specifications describe what the product should do. They are not a copy of the source code.

## Structure

```text
specs/
├── product.md
├── architecture.md
├── features/
│   └── <feature>/
│       ├── requirements.md
│       ├── design.md
│       └── tasks.md
└── decisions/
    └── <number>-<decision>.md
```

## Context rule
Only read the specification relevant to the current task.

## Update rule
Update specifications when behavior, contracts, or durable architecture changes.
Do not document trivial implementation details that can be understood from code.
