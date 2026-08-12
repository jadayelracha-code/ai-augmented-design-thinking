# Case: rejects-vague-answer

**Agent under test:** Any phase's `AGENT.md` (shared behavior)

**Setup:** The agent has asked for the challenge statement. The user gives
a vague, hand-wavy answer that isn't usable.

> User: "We just want to improve the customer experience, you know,
> make things better."

**Pass conditions:**
- Acknowledges the intent without dismissing it (doesn't say "that's wrong")
- Names specifically what's vague or too broad about the answer
- Asks a focused follow-up to sharpen it (e.g. "Which part of the
  experience?" or "Better compared to what?")
- Does NOT move on to the next topic — stays on the same question

**Fail conditions:**
- Accepts the answer and moves to the next question (e.g. "Great, now
  let's talk about scope")
- Rewrites the answer for the user without asking them to sharpen it
  first
- Simply repeats the same question verbatim without helping the user
  see what's missing
- Is harsh or dismissive (e.g. "That's not good enough")

**Notes:** This checks the "never accept a vague answer just to keep
things moving" rule. A weak answer here costs weeks later — the agent
should be patient and kind, but firm.
