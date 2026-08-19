# ExFu Humane Agents

> `exfu-humane-agents` · <https://github.com/ExFu/humane-agents>

Conventions for the human–agent interface.

Agent output is optimised for correctness and completeness — which, left
unattended, means it is optimised *against* human cognition: dense, long,
referential, jargon-saturated. The humans reading it are time-poor, don't
share the agent's context, cannot resolve its references, and may have ADHD
or other reasons to struggle with long complicated text.

**Humane agents are agents designed around human limits — attention, working
memory, context — not agents that perform humanity.** This plugin ships that
principle as installable conventions: skills that change how an agent
communicates, with zero loss of rigour on the agent-facing record.

## What's here

- **`plugins/exfu-humane-agents/`** — the plugin source. One skill so far:
  - `exfu-reporting` — dual-audience reporting. Every report is two
    artifacts: an **Agent Report** (rich, strict, complete — golden-circle
    Why/How/What, resolvable references) and a **Human Report** (≤250 words,
    plain words, narrative, leads with the outcome), derived by translation,
    not truncation.
- **`planning/`** — the tiered plan corpus (ExFu Planning Methodology);
  `T1-top-level.md` carries the full thesis and roadmap.
- **`.apv/`** — the append-only event log; this repo is tracked by
  agent-plan-visualiser.

## The admission rule

A skill enters this plugin only if it (a) improves the human–agent
interface, and (b) depends on nothing from the ExFu planning/delegation/APV
stack — every convention here is usable standalone, by anyone. Anything
methodology-coupled belongs in those plugins instead. This rule is what
keeps the plugin a thesis rather than a drawer.

## Roadmap (sketch — see `planning/T1-top-level.md`)

- **Communication**: reporting (shipped) → progress narration →
  notification/summary conventions.
- **Interaction**: question batching and decision elicitation that doesn't
  overwhelm.
- **Mechanisms**: a fresh-context report reviewer — a subagent spawned cold
  can't resolve the session's jargon, so it catches unexplained references
  *by construction* (the curse of knowledge, inverted into a detector).

## Installing

Distribution through the common `exfu` marketplace (entry pending):

```bash
claude plugin marketplace add https://github.com/ExFu/exfu-marketplace.git
claude plugin install exfu-humane-agents@exfu
```

## License

Proprietary — see [LICENSE](LICENSE). This repository is public for
distribution convenience; publication does not grant an open-source licence.
Redistribution enquiries: al@exfu.ai
