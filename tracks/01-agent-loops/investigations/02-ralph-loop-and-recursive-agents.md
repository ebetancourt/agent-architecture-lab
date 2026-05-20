# Ralph Loop and Recursive Agents

## Objective

Study Ralph-style coding loops as the smallest useful orchestration pattern: repeat an agent invocation against durable external state until a completion condition is met.

## Why This Matters

The Ralph pattern strips agent architecture down to a blunt control loop. It makes the boundary between model reasoning, runtime orchestration, file-system memory, and verification unusually visible.

## Systems / Resources

- [Geoffrey Huntley bio](https://ghuntley.com/bio/)
- [Ralph Loops format proposal](https://ralphloops.io/)
- [Ralph Loop runtime example](https://ralphloop.sh/)
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)

## Investigation Tasks

- Identify the loop boundary: prompt load, agent invocation, file changes, validation, next iteration.
- Map which state persists through files, git, task lists, logs, and checkpoints.
- Inspect how retry behavior emerges from deterministic wrapper logic plus nondeterministic model output.
- Compare "fresh context per iteration" with conversational continuity.
- Identify failure modes: drift, unchecked commits, repeated bad fixes, partial task completion, cost runaway.

## Architectural Questions

- What makes the loop recursive rather than merely repeated?
- Where is memory located when the model context is discarded each iteration?
- How is completion determined?
- What does the runtime need to observe before deciding to continue?
- Which safeguards belong in the wrapper rather than the agent prompt?

## Reconstruction Ideas

- Sketch a file-backed task loop with explicit done conditions and validation commands.
- Add checkpointing and rollback as runtime behavior, not model instructions.
- Compare a bash-style loop with a small evented runtime that records iteration metadata.

## Deliverables

- Runtime loop diagram.
- State persistence map.
- Risk notes for unattended loop execution.

## Reflection Notes

To be filled during investigation.
