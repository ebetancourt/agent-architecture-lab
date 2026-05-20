# Coding Agent Loop Diagram

## Generic Loop

```mermaid
sequenceDiagram
    participant U as User
    participant R as Runtime
    participant C as Context Assembler
    participant M as Model
    participant T as Tools
    participant W as Workspace

    U->>R: Request or steering input
    R->>W: Inspect workspace state
    R->>C: Build task context
    C->>M: Prompt, files, history, constraints
    M->>R: Proposed plan or action
    R->>T: Execute approved action
    T->>W: Read, edit, run, browse
    W-->>T: Result
    T-->>R: Observation
    R->>R: Evaluate result
    alt Continue
        R->>C: Add observation and iterate
    else Ask user
        R->>U: Surface decision point
    else Complete
        R->>U: Final result and trace
    end
```

## Execution Observations

- The runtime is the control surface; the model is not the whole agent.
- Context assembly is a loop boundary because it decides what the model can reason over.
- Tools convert model intent into observable state changes.
- Evaluation should use external evidence whenever possible.
- User control is part of the architecture, not an afterthought.

## Trace Refinements

- Add explicit retry and rollback paths.
- Add separate planning and execution model calls where systems support them.
- Add sandbox lifecycle events for hosted runtimes.
