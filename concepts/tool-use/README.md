# Tool Use

## Definition

Tool use is the structured handoff between model intent and external capabilities such as shells, file systems, browsers, APIs, and hosted runtimes.

## Architectural Notes

- Tool contracts should define inputs, outputs, side effects, and failure modes.
- Tool results become observations for the next loop iteration.
- Dangerous tools need permission boundaries and traceability.
