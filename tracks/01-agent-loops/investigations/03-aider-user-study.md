# Aider User Study

## Objective

Study Aider as an interactive coding-agent interface where the loop is mediated through chat, repository state, diffs, and test feedback.

## Why This Matters

Aider exposes a compact, practical version of the coding-agent loop. The user can see how files enter context, how edits are proposed, how git state matters, and how verification can be folded back into the interaction.

## Systems / Resources

- [Aider docs](https://aider.chat/docs/)
- [Aider GitHub repository](https://github.com/Aider-AI/aider)
- [Aider usage guide](https://aider.chat/docs/usage.html)

## Investigation Tasks

- Observe how files are selected or added to context.
- Trace how a user request becomes an edit proposal.
- Inspect the role of git state, diffs, and commit behavior.
- Record how test or command output changes the next model turn.
- Identify where the user remains responsible for judgement, approval, or correction.

## Architectural Questions

- What constitutes one loop iteration in an interactive chat agent?
- Where does planning occur: explicit response text, hidden prompt structure, or edit strategy?
- What persists across turns?
- How is repository context narrowed?
- How does the interface keep the user in control?

## Reconstruction Ideas

- Rebuild a minimal edit loop around a prompt, selected files, generated patch, and verification command.
- Add a "diff as observation" event type to a simple trace schema.
- Compare manual file selection with automatic repository mapping.

## Deliverables

- Interaction trace from request to diff.
- Notes on context selection and git-state coupling.
- Small diagram of user-agent-runtime responsibilities.

## Reflection Notes

To be filled during investigation.
