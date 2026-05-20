# Reflection Loop

## Purpose

Explore whether adding an evaluator step improves loop reliability or merely adds another place for the model to sound confident.

## Architectural Focus

- Separation between actor and evaluator roles.
- Evaluation criteria as runtime policy.
- Retry decisions after failed commands or suspicious patches.
- Distinguishing self-critique from externally grounded verification.

## Constraints

- Reflection must inspect concrete artifacts: diff, command output, trace events, or failing tests.
- The evaluator cannot approve work without evidence.
- Retry count and escalation behavior must be explicit.

## Implementation Sketch

1. Run a normal loop iteration.
2. Capture the proposed action and resulting observation.
3. Evaluate against a small checklist: goal alignment, safety, verification, unresolved errors.
4. Choose continue, retry with constraints, ask user, or stop.
5. Record the evaluator decision as part of the trace.

## Observations

- To be filled during experiment runs.

## Future Extensions

- Compare single-model reflection with a separate evaluator call.
- Add rule-based checks before model evaluation.
- Track whether reflection prevents repeated failures or only delays them.
