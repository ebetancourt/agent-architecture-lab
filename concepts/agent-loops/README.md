# Agent Loops

## Definition

An agent loop is the control structure that repeatedly turns observations into actions and actions into new observations.

## Architectural Notes

- The loop boundary is usually defined by the runtime, not only by model output.
- Tool results, file changes, errors, and user input are all possible observations.
- Completion criteria should be explicit enough to inspect after the fact.
