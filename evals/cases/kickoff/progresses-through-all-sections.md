# Case: progresses-through-all-sections

**Agent under test:** [`kickoff/AGENT.md`](../../../kickoff/AGENT.md)

**Setup:** Full Kick Off conversation. The user gives reasonable (not
perfect, but usable) answers to each question. The conversation should
be long enough for the agent to reach all six sections.

> User gives a clear-enough challenge, engages with scoping, and answers
> follow-ups without being evasive.

**Pass conditions:**
- Covers all six Kick Off sections by the end of the conversation:
  1. The Challenge (challenge statement)
  2. Scoping (in/out/ambiguous)
  3. The Team (multidisciplinary check, solo practitioner handling)
  4. Stakeholders (stakeholder map, influence/interest)
  5. Getting Oriented (concept map, charette)
  6. Readiness Check (honest verdict before moving to Understand)
- Moves to the next section once the current one is genuinely answered —
  does not over-probe a section that's already solid enough
- Tracks progress lightly so the user feels momentum

**Fail conditions:**
- Gets stuck on one section (e.g. challenge sharpening) and never
  reaches the later sections (team, stakeholders, concept map, charette)
- Skips sections entirely without the user asking to skip
- Moves on from a section that's still vague or unanswered
- Over-probes a section that's already been answered well enough,
  effectively blocking progress through the rest of the Kick Off

**Notes:** This is a coverage test. The other kickoff cases test specific
behaviors (stay in lane, etc.) — this one checks that the agent actually
completes the full coaching sequence. The live dry run on 2026-08-12
surfaced this: the agent over-probed the challenge statement and never
reached team, stakeholders, concept map, or charette.
