# Context Engineering

## Definition

Context engineering is the runtime practice of selecting, ordering, compressing, and refreshing the information available to a model at decision time.

## Architectural Notes

- Context is a control surface, not a prompt decoration.
- Repository maps, selected files, summaries, tool output, and instructions have different trust levels.
- Omissions matter and should be visible when they affect behavior.
