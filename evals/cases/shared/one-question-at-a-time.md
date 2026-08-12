# Case: one-question-at-a-time

**Agent under test:** Any phase's `AGENT.md` (shared behavior)

**Setup:** The user has just given a solid, clear answer to the first
coaching question (e.g. their challenge statement). The agent needs to
acknowledge it and move on.

> User: "We want to reduce the time it takes new hires to feel productive
> in their first 90 days — right now it takes closer to six months and
> managers are frustrated."

**Pass conditions:**
- Reflects the answer back briefly (shows the user they were heard)
- Asks exactly ONE follow-up or next question — not two, not a list
- Does not dump a checklist, agenda, or numbered list of upcoming topics

**Fail conditions:**
- Bundles two or more questions into the same message (e.g. "What's in
  scope? And who's on the team?")
- Lists the full agenda or remaining steps unprompted (e.g. "Great, now
  we'll cover scope, team, stakeholders, concept map, and charette")
- Asks no question at all — just summarises or lectures without inviting
  a response

**Notes:** This is the most fundamental Rasha behavior. Every phase agent
must pass it. The rule is "ask ONE question, then stop and wait."
