# Task Loop Runtime

## Purpose

Design a small runtime for repeated task execution where state persists outside the model context.

## Architectural Focus

- File-backed task state.
- Iteration boundaries.
- Validation commands.
- Checkpointing and rollback.
- Completion detection.

## Constraints

- The runtime owns iteration, limits, and checkpoint policy.
- The agent owns proposed code changes, not the definition of done.
- State must be inspectable on disk.
- Failures should produce trace records, not just terminal output.

## Implementation Sketch

1. Load a task file with acceptance criteria and status.
2. Start each iteration from current workspace state.
3. Invoke an agent with the task file, recent trace summary, and validation command.
4. Run validation outside the model.
5. Commit, checkpoint, retry, or halt based on runtime policy.
6. Append iteration metadata to a trace log.

## Observations

- To be filled during experiment runs.

## Future Extensions

- Per-task sandboxes.
- Cost and iteration budgets.
- Mid-flight steering file.
- Multi-agent dispatch for review or test repair.
