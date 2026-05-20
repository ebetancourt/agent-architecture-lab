# Token Budgeting

## Objective

Study how token limits force architectural choices about relevance, ordering, summarization, and omission.

## Architectural Questions

- What should be dropped first when context is too large?
- How should the runtime expose context omissions?
- Which loop events deserve durable summaries?

## Systems / Resources

- [Claude Code docs](https://code.claude.com/docs)

## Future Exploration

- Build a context budget ledger for one agent trace.
- Compare naive truncation with policy-driven pruning.

## Notes

To be filled during future exploration.
