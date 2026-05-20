# OpenHands Execution Model

## Objective

Study OpenHands as a broader software-agent runtime where planning, execution, sandboxing, UI, and tool use are more explicitly separated.

## Why This Matters

OpenHands is useful for understanding agent loops that run inside a richer execution environment. It exposes concerns that smaller terminal agents can hide: event streams, sandbox lifecycle, browser or shell actions, delegation between frontend and backend, and persistent task state.

## Systems / Resources

- [OpenHands docs](https://docs.openhands.dev/)
- [OpenHands GitHub repository](https://github.com/OpenHands/OpenHands)
- [OpenHands paper](https://arxiv.org/abs/2407.16741)

## Investigation Tasks

- Trace the request lifecycle through UI, backend runtime, sandbox, and tool execution.
- Identify the event model used to represent agent actions and observations.
- Map where planning, execution, evaluation, and user control appear.
- Inspect how sandbox state is created, reused, or discarded.
- Compare OpenHands' execution loop with terminal-first agents such as Aider.

## Architectural Questions

- What is the runtime's unit of work?
- Where does orchestration live?
- How are actions represented before and after execution?
- What persists across task boundaries?
- How does the system expose enough trace data for debugging?

## Reconstruction Ideas

- Sketch a minimal event stream for plan, action, observation, and completion.
- Rebuild a small sandbox-backed loop interface on paper before implementing anything.
- Compare an evented runtime with a synchronous command-response loop.

## Deliverables

- Runtime component diagram.
- Request lifecycle trace.
- Notes on event representation and sandbox boundaries.

## Reflection Notes

To be filled during investigation.
