# Agent Loops Notes

## Observations

- Coding-agent loops are legible because they leave artifacts: diffs, command output, logs, commits, traces, and failed tests.
- The runtime defines the practical loop boundary more than the prompt does.
- File systems and git often behave as memory even when a system does not describe them that way.
- Completion is an architectural decision: model-declared done, test success, user approval, budget exhaustion, or runtime policy.

## Synthesis Prompts

- Which loop model is most useful for coding agents?
- What information should be captured at each loop boundary?
- Which loop events should be first-class trace records?
- When should the runtime override the model's preferred next action?

## Follow-Ups

- [ ] Convert useful loop patterns into diagrams.
- [ ] Compare Aider and OpenHands request lifecycles.
- [ ] Define a minimal trace schema for `mini-agent-v0`.
