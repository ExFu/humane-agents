---
id: T1-top-level
plan_kind: thematic
tier: 1
status: active
---

# T1-top-level — ExFu Humane Agents — Top-level plan

**Status**: Accepted 2026-08-18 by the operator (ceremony recorded in the
event log; Q1–Q4 left open at acceptance). Authored 2026-08-18 (Claude Code
session, from the operator's direction in the agent-planning-and-delegating
repo where the first convention was built).

---

## 1. Why

Agents now mediate a growing share of knowledge work, and the interface
between agents and humans is systematically neglected. Agent output is
optimised for correctness and completeness — which, unattended, produces
prose optimised *against* human cognition: dense, long, referential,
jargon-saturated. The humans on the receiving end are time-poor, don't share
the agent's working context, cannot resolve its references, and may have ADHD
or other reasons to struggle with long complicated text. The operator cares
about this interface more than most and thinks about it deliberately; this
project is where that thinking becomes shippable.

**The thesis**: humane agents are agents designed around human limits —
attention, working memory, context — not agents that perform humanity.
This is a psychological project, not a cosmetic one: it is about what
reaches a human mind intact, not about tone or persona.

**Success looks like**: installing this plugin measurably changes how an
agent communicates — reports arrive readable, questions arrive answerable,
progress arrives glanceable — with zero loss of rigour on the agent-facing
record. Each convention is usable standalone by anyone, inside or outside
the ExFu stack. The audience is any operator of agentic tooling, starting
with the operator's own projects.

## 2. How

- **Skills-as-conventions.** Each convention ships as one self-contained
  skill. Admission rule: a skill enters this plugin only if it improves the
  human–agent interface AND depends on nothing from the planning/delegation/
  APV stack. Anything methodology-coupled belongs in those plugins instead.
- **Dual-audience separation is the recurring pattern.** Agent-facing rigour
  and human-facing accessibility are contradictory optimisation targets;
  conventions resolve the contradiction by producing separate artifacts or
  registers, never by compromising one target for the other.
- **Evidence-driven authoring.** Every convention is written against a
  demonstrated baseline failure (the skill-writing RED/GREEN discipline):
  observe the undesired behaviour without the skill, write the skill to
  target those specific failures, verify behaviour changes with it.
- **Distribution** through the common `exfu` marketplace as a proper plugin
  with its own identity and versioning.

## 3. What — themes

Each theme becomes a T2 when work on it begins.

- **Communication** — the artifacts agents emit for humans: reports (first,
  shipped), progress narration, notifications, summaries. → `T2-communication`
  (spawned 2026-08-18).
- **Interaction** — how agents take input from humans: question batching and
  timing, interruption etiquette, elicitation of decisions without
  overwhelming. (future T2)
- **Mechanisms** — structural tools that exploit agent architecture for
  humane outcomes, e.g. a fresh-context report reviewer that catches
  unexplained jargon *by construction* (a cold subagent literally cannot
  resolve the session's references — the curse of knowledge, inverted into
  a detector). (future T2)

## Milestones (sketch)

- **M1 — first shipped convention**: the plugin exists, installs from the
  marketplace, and ships `exfu-reporting` with its evidence trail.
  → `M1-first-convention` (instantiated 2026-08-18).

## 4. Open questions (HITL)

- **Q1 — reviewer-agent mechanism.** Does the fresh-context report reviewer
  earn a shipped agent definition in this plugin, and if so at what point
  (after how much dogfood evidence on `exfu-reporting`)?
- **Q2 — per-surface variants.** Do conventions need surface-specific
  variants (CLI vs Cowork/Desktop vs chat) or does one skill per convention
  hold everywhere?
- **Q3 — relationship to the planning stack.** Should
  `exfu-agent-planning-and-delegating` (and APV's reporting surfaces) come to
  *depend* on this plugin for report format, or only recommend it? Direction
  of dependency is a real architectural choice.
- **Q4 — licensing posture.** Siblings are proprietary; these conventions
  arguably spread further (and serve the thesis better) under a permissive
  licence. Operator ruling needed; LICENSE file deferred until then.

## 5. Rulings (2026-08-19)

- **Q4 (licensing posture)**: same licence as the other ExFu plugins —
  the proprietary licence (public repo for distribution convenience, no
  open-source grant; its §7 explicitly permits a later open-source
  re-release, so the permissive option stays open without blocking now).
  LICENSE file added same day. Q1–Q3 remain open.
