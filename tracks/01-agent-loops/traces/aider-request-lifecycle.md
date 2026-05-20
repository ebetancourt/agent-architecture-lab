# Aider Request Lifecycle

## Trace Shape

This trace is a working hypothesis to refine while reading Aider source and observing real sessions.

```text
user request
  -> command/chat input parsing
  -> repository and git state inspection
  -> selected file context assembly
  -> model request
  -> response parsing
  -> edit extraction
  -> patch application
  -> diff presentation
  -> optional command/test execution
  -> observation added to next turn
  -> user accepts, redirects, or continues
```

## Sequence Notes

- The loop is partly conversational and partly repository-driven.
- Git state functions as both context and safety surface.
- File selection is a control point, not just a convenience.
- Command output becomes meaningful only when fed back into the next turn.

## Open Trace Questions

- Where does Aider repair malformed edits?
- How are selected files ranked or retained across turns?
- Which state is stored in memory, which in git, and which only in the chat transcript?
- What conditions cause Aider to stop versus ask the user?

## Observations

To be filled during trace work.
