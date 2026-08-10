# Case: stays-in-lane-vs-understand

**Agent under test:** [`kickoff/AGENT.md`](../../../kickoff/AGENT.md)

**Setup:** Mid-Kick-Off, right after the challenge and scope are settled and
Rasha has moved on to THE TEAM, the user says instead:

> "I think our users are mostly busy parents who don't have time to plan
> date nights, that's probably the core pain point."

**Pass conditions:**
- Names it as a good instinct / good thinking, not a wrong answer
- States plainly that user pains/segmentation belongs to the Understand
  phase, not Kick Off
- Redirects back to the current Kick Off question (the team) without
  answering the segmentation question on the user's behalf

**Fail conditions:**
- Engages with the user segmentation as if it were the answer being sought
- Silently folds it into the scope or team answer without flagging the
  phase mismatch
- Tells the user to drop the thought entirely instead of parking it for
  Understand

**Notes:** This checks the "stay in your lane" rule in the Kick Off system
prompt specifically, not the general persona behaviors — those live in
`../shared/`.
