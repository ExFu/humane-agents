---
id: T3-reporting-skill
plan_kind: thematic
tier: 3
t2_parent: T2-communication
milestone: M1-first-convention
status: draft
---

# T3-reporting-skill — ship the dual-audience reporting convention

**Status**: Draft, **retrospective**: this brief documents work already
implemented on 2026-08-18 (originally on branch
`claude/dual-format-reporting-skill-dae67d` of the
`agent-planning-and-delegating` repo, transplanted here when the operator
ruled this project into existence). It is written executable-cold anyway so
the record of what was built, and how it was verified, survives without
conversational context. Awaiting operator acceptance; on acceptance the
completion events for this work can be recorded.

## Task

Ship a skill `exfu-reporting` at
`plugins/exfu-humane-agents/skills/exfu-reporting/SKILL.md` implementing
dual-audience reporting per T2-communication principle 1:

- Frontmatter: `name: exfu-reporting`; `description` starting "Use when",
  trigger-only (no workflow summary), covering: completion reports, status
  updates, milestone reports, audit summaries, handoff summaries, "write
  up / report on / summarise" requests, mixed human+agent readership, and
  complaints that an existing report is dense/jargon-heavy.
- Body: two-artifact rule (Agent Report + Human Report, never one);
  Agent Report spec (golden-circle Why/How/What sections, strict
  terminology, resolvable references, complete coverage, workflow state
  included); Human Report spec (outcome-first, narrative golden circle,
  zero unexplained jargon with the day-one-outsider test, no internal
  workflow mechanics beyond a single takehome line, ≤250-word budget,
  caveats survive translation); derivation rule (agent first, human derived
  by translation not truncation); filing convention (`<name>.md` human /
  `<name>.agent.md` agent, human gets the discoverable name, human report
  links the agent one; chat delivery leads with the human version); common
  mistakes table.

## Verification (executed 2026-08-18, both green)

Method: skill-writing RED/GREEN discipline, via a subagent given identical
raw working notes (a realistic migration scenario with internal jargon,
a delegated audit, deferred items).

1. **RED (baseline, no skill)**: subagent produced one dense report —
   opened with branch/plan metadata, no Why, unresolved jargon throughout,
   workflow ceremony mixed with substance, no human-oriented variant.
   Pass criterion for the skill: these specific failures targeted in its text.
2. **GREEN (with skill)**: same scenario produced both artifacts; human
   report led with the outcome, ~230 words, jargon translated or cut,
   workflow collapsed to one line, caveats intact; agent report carried
   Why/How/What and flagged its own unresolvable references as defects.
   Pass criterion met: every RED failure absent.

Re-verification after any future edit to the skill: rerun both scenarios
(the raw notes are reusable; any realistic jargon-dense scenario serves)
and require the same pass criteria.

## Out of scope

- The fresh-context reviewer agent (T1 Q1) — mechanism, not this convention.
- Progress narration and notifications (T2-communication U2/U3).
- Any dependency on planning/delegation/APV constructs inside the skill text
  (admission rule, T1 §2).
