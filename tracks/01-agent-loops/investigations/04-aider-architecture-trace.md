# Aider Architecture Trace

## Objective

Reverse engineer Aider's loop structure from its documentation and source code, focusing on control flow rather than feature inventory.

## Why This Matters

Aider is open enough to study as a real implementation. Its architecture can reveal how a mature coding agent handles repository state, model calls, edit formats, command execution, and user interaction without requiring speculative reconstruction.

## Systems / Resources

- [Aider GitHub repository](https://github.com/Aider-AI/aider)
- [Aider docs](https://aider.chat/docs/)
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)

## Investigation Tasks

- Locate the main interaction loop and identify its inputs and outputs.
- Trace request handling from user message through context construction and model call.
- Identify edit application boundaries and failure handling.
- Inspect how repository metadata, git state, and selected files are represented.
- Look for retry, repair, or fallback logic around malformed edits and command failures.

## Architectural Questions

- What is the smallest unit of loop state?
- Which responsibilities are runtime concerns versus model concerns?
- How does the system decide that an edit is valid enough to apply?
- What observations are fed back into the next iteration?
- Where are policy decisions encoded?

## Reconstruction Ideas

- Draw a call graph for one request lifecycle.
- Extract a minimal event schema from Aider's loop: input, context, model response, edit, command, observation.
- Recreate one edit-apply-repair path in pseudocode.

## Deliverables

- Source-informed request lifecycle trace.
- Boundary map for context, model, editor, git, and shell.
- Notes on repair and retry behavior.

## Reflection Notes

To be filled during investigation.
