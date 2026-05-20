# Multi-Agent Systems

## Definition

A multi-agent system distributes work across multiple model-driven roles, workers, reviewers, or orchestrated execution contexts.

## Architectural Notes

- Delegation introduces coordination state and merge points.
- Parallelism is useful only when subtasks have clean boundaries.
- Review agents need independent evidence, not just a second opinion.
