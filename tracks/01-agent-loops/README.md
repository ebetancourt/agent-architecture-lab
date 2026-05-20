# Agent Loops

Coding agents are a useful entry point into agent architecture because their work is concrete, inspectable, and constrained by external reality. They read files, modify code, run tools, observe failures, and either recover or stop. The loop is not an abstraction floating above the system; it is visible in command history, patches, test output, traces, and user interruptions.

Loops matter because they define how an agent turns intent into progress. The interesting questions are not whether a loop exists, but where it starts, where state persists, how tool results alter control flow, and how completion is decided.

Coding agents also expose runtime architecture unusually clearly. Their behavior depends on workspace boundaries, context assembly, tool permissions, sandboxing, retry policy, and human review. Small differences in runtime design create large differences in agent behavior.

## Architectural Primitives

- Observation: what the agent can see before acting.
- Context assembly: how task, code, memory, and instructions enter the model call.
- Planning: where intent becomes an ordered action strategy.
- Tool execution: how shell, file, browser, and API calls are mediated.
- Evaluation: how the system decides whether work succeeded.
- Persistence: what survives between iterations.
- Control: how users interrupt, approve, steer, or review work.

## Investigations

- [ ] [Amp anatomy of a coding agent](investigations/01-amp-anatomy-of-a-coding-agent.md)
- [ ] [Ralph loop and recursive agents](investigations/02-ralph-loop-and-recursive-agents.md)
- [ ] [Aider user study](investigations/03-aider-user-study.md)
- [ ] [Aider architecture trace](investigations/04-aider-architecture-trace.md)
- [ ] [OpenHands execution model](investigations/05-openhands-execution-model.md)

## Experiments

- [ ] [Mini agent v0](experiments/mini-agent-v0.md)
- [ ] [Reflection loop](experiments/reflection-loop.md)
- [ ] [Task loop runtime](experiments/task-loop-runtime.md)

## Traces

- [Aider request lifecycle](traces/aider-request-lifecycle.md)
- [Coding agent loop diagram](traces/coding-agent-loop-diagram.md)

## Open Questions

- Where does planning actually occur: model output, runtime policy, tool affordances, or user steering?
- What counts as loop state when context, files, git, shell history, and summaries all influence behavior?
- How should a runtime decide between retry, escalation, rollback, and completion?
- Which loop boundaries should be observable to the user?

## Related Systems

- Aider
- OpenHands
- Claude Code
- Amp
- Ralph-style loop wrappers

## Notes

- [Track notes](notes.md)
