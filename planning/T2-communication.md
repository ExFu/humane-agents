---
id: T2-communication
plan_kind: thematic
tier: 2
status: active
---

# T2-communication — Communication theme — what agents emit for humans

**Status**: Accepted 2026-08-18 by the operator (ceremony recorded in the
event log). Spawned from `T1-top-level` §3 (theme: Communication) on
2026-08-18, instantiated because work on the theme had already begun (the
reporting convention).

## 1. Why (inherited, condensed)

Per T1 §1: agent output is optimised against human cognition by default.
This theme owns the emission side of the interface — everything an agent
writes *for a human to read*.

## 2. Principles

1. **Dual-audience separation.** A communication artifact serves either
   agent consumption or human consumption, never both at once. Where both
   audiences exist, produce two artifacts; derive the human one from the
   agent one by translation, not truncation. (Realised first in
   `exfu-reporting` — the skill text is the authoritative statement of the
   reporting-specific rules; this T2 does not restate them.)
2. **Outcome first.** Human-facing artifacts lead with the takehome; metadata
   and mechanism follow or are cut.
3. **Budgets are hard.** Human-facing artifacts carry explicit length
   budgets. Exceeding a budget is a defect, not a style choice — importance
   beyond the budget belongs in the agent-facing artifact.
4. **Jargon zero-tolerance test.** Every sentence of a human-facing artifact
   must be intelligible to a smart outsider on day one; internal terms are
   translated or cut.
5. **Caveats survive translation.** Accessibility never launders
   uncertainty, risk, or bad news into smoothness.

## 3. Units

- **U1 `exfu-reporting`** — dual-audience reporting (Agent Report + Human
  Report). Shipped v0; see `T3-reporting-skill`.
- **U2 progress narration** — how long-running work reads from the outside
  (glanceable status, not log spam). Future; needs its own baseline evidence.
- **U3 notifications/summaries** — when to surface, at what length, with
  what lead. Future.

## Glossary

- **Agent Report** — the rich, strict, complete artifact for machine/agent
  consumption.
- **Human Report** — the short, plain, narrative artifact for time-poor
  humans; derived from the Agent Report.
- **Takehome** — the one thing a busy reader must retain; what a human-facing
  artifact leads with.
