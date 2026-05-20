# Amp: Anatomy of a Coding Agent

## Objective

Use Amp as a product-facing reference point for studying how a coding agent presents a loop, shares state, and exposes collaboration surfaces.

## Why This Matters

Amp is useful here not because its internals are fully visible, but because its user-visible behavior highlights architectural pressure points: context depth, thread sharing, tool orchestration, subagent-style delegation, and long-running work.

## Systems / Resources

- [Amp](https://sourcegraph.com/amp)
- [Sourcegraph: why Sourcegraph and Amp are becoming independent companies](https://sourcegraph.com/blog/why-sourcegraph-and-amp-are-becoming-independent-companies)
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)

## Investigation Tasks

- Trace the visible loop from request intake to proposed code changes.
- Identify which surfaces expose planning, progress, tool use, and completion.
- Compare single-thread interaction with shareable or persistent thread behavior.
- Look for evidence of specialized subflows: code search, library research, review, or parallel analysis.
- Record what appears to live in product runtime versus model prompt.

## Architectural Questions

- What constitutes the loop from the user's perspective?
- Where does orchestration appear to live?
- Which parts of context are local, shared, or durable?
- How does the system communicate uncertainty or partial progress?
- What assumptions are hidden behind the product interface?

## Reconstruction Ideas

- Model a minimal "thread as trace" representation for a coding-agent loop.
- Sketch a runtime that records planning, tool calls, file edits, and completion checks as first-class events.
- Compare a single-agent loop with a loop that delegates code search to a separate analysis pass.

## Deliverables

- Product-surface loop diagram.
- Notes on visible versus inferred runtime boundaries.
- Short comparison with Aider or Claude Code once those traces exist.

## Reflection Notes

To be filled during investigation.
