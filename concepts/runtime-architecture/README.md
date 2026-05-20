# Runtime Architecture

## Definition

Runtime architecture is the execution environment that mediates model calls, context assembly, tool use, permissions, state, traces, and user control.

## Architectural Notes

- The runtime decides what the agent can observe and mutate.
- Sandboxes, workspaces, tool contracts, and approval gates shape behavior.
- Traceability is part of runtime design, not a logging afterthought.
