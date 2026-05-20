# Prompt Layering

## Objective

Study how system instructions, repository conventions, user requests, tool results, and runtime policy are layered.

## Architectural Questions

- Which instruction layers are durable?
- Which layer wins during conflict?
- Should prompt construction be visible in traces?

## Systems / Resources

- [Claude Code docs](https://code.claude.com/docs)
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)

## Future Exploration

- Map instruction layers for a real coding-agent session.
- Identify instructions that belong in runtime policy rather than prompt text.

## Notes

To be filled during future exploration.
