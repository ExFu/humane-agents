---
name: exfu-reporting
description: Use when writing up completed work as a durable artifact - a completion report, status update, milestone report, audit summary, handoff summary, or any "report on / write up / summarise what happened" request. Also use when a report will be read by both humans and agents, or when an existing report is criticised as dense, jargon-heavy, or hard to read.
---

# exfu-reporting — dual-audience reporting

Every report is **two artifacts, never one**: an **Agent Report** (rich, strict, complete — for machine/agent consumption) and a **Human Report** (short, plain, narrative — for time-poor humans). One report cannot serve both audiences: optimising for agent completeness produces exactly the dense, referential prose humans cannot read, and optimising for readability drops the precision agents need. Write the Agent Report first; **derive** the Human Report from it by *translation, not truncation*.

## The Agent Report

Audience: future agent sessions, delegates, auditors — context-free readers with perfect tolerance for density.

- **Golden circle, explicit sections.** *Why* — what this work was for, tied to the governing intent (plan IDs, milestone). *How* — approach taken, constraints honoured, decisions made and their rationale. *What* — the complete change inventory, evidence, and resulting state.
- **Strict terminology.** Exact IDs, exact file paths, exact command/tool names. Never paraphrase an identifier.
- **Resolvable references.** Every ID or artifact named must carry enough to resolve it (path, plan ID, ticket ref). "Ticketed" without a ref is a defect.
- **Complete and correct coverage.** All work done, all findings and their dispositions, verification evidence (what was run, what it showed), everything deferred or left open — with owner/next-step. Omissions are the failure mode here, not length.
- **Workflow state belongs here.** Capture/gate/ceremony status (e.g. APV captures, gate colour, pending merge ceremony) is agent-relevant: record it fully.

## The Human Report

Audience: a time-poor reader who does not know the project's jargon, cannot resolve references, and may have ADHD or otherwise struggle with long, complicated text. They are reading for **orientation and executive takehomes**, not implementation detail. Anyone needing depth reads the Agent Report — link it and let go of completeness.

Rules:

- **Lead with the outcome.** First sentence = the single takehome a busy reader needs. Never open with metadata, IDs, or scope preamble.
- **Narrative golden circle.** A few short paragraphs telling the story: why this mattered → what was done (plain words) → what it means now / what happens next. Story order, not section-heading order.
- **Zero unexplained jargon.** Every acronym, codename, or internal term is either translated into plain words or cut. Test: would a smart outsider on their first day understand every sentence? Plan IDs and internal tooling names usually just get cut.
- **No internal workflow mechanics.** Capture counts, gate states, ceremony names, delegation billing — collapse to the takehome only ("all work is tracked and independently audited"), or omit.
- **Hard budget: ≤ 250 words / one screen.** Short sentences. Short paragraphs (1–3 sentences). At most one small bullet list. Bold the 2–4 phrases a skimmer must catch.
- **Caveats survive translation.** If something is unfinished, risky, or awaiting sign-off, the human report must say so plainly — readability never launders uncertainty into "done".

## Filing

File the pair together; the human report gets the discoverable name: `<name>.md` (human) and `<name>.agent.md` (agent), in the repo's reports location (or wherever the requester specifies). The human report links its agent counterpart in a final line: *"Full technical report: `<name>.agent.md`."* When a report is delivered in chat rather than filed, give the Human Report as the message and attach/append the Agent Report — never the reverse.

## Common mistakes

| Mistake | Fix |
|---|---|
| One report "for everyone" | Always two artifacts; they have contradictory optimisation targets |
| Human report = compressed agent report | Compression keeps the jargon; translate instead — rewrite in plain words |
| Leading with branch/plan/metadata | Outcome first; metadata lives in the Agent Report |
| "Why" missing entirely | Both reports carry Why; agents need it as grounding, humans as story |
| Unresolvable refs ("ticketed", "queued") | Agent report: attach the ref. Human report: plain-words consequence or cut |
| Workflow ceremony detail in the human report | One plain-words takehome line, or nothing |
| Human report over budget "because it's all important" | It isn't; importance beyond the takehomes lives in the Agent Report |
| Softening bad news in the human report | Plain words ≠ good news; caveats and failures stated plainly |
