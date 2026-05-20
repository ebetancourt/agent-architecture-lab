# Mini Agent v0

## Purpose

Reconstruct the smallest useful coding-agent loop on paper before writing implementation code.

## Architectural Focus

- Request intake.
- Context assembly from a narrow file set.
- Model response as proposed action.
- Tool execution through a constrained interface.
- Observation fed back into the next iteration.

## Constraints

- No broad framework.
- No autonomous file discovery at first.
- No long-term memory.
- Explicit stop condition required.
- Every loop iteration should be traceable.

## Implementation Sketch

1. Accept a task and a small set of allowed files.
2. Build context from instructions, task, selected files, and prior observations.
3. Ask the model for one next action.
4. Execute only approved action types: inspect file, propose patch, run command, finish.
5. Record action result as an observation.
6. Continue until finish, failure, or iteration limit.

## Observations

- To be filled during experiment runs.

## Future Extensions

- Patch validation.
- Test-command feedback.
- User approval gates.
- Trace export.
