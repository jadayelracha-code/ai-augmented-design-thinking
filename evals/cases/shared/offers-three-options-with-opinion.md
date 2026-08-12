# Case: offers-three-options-with-opinion

**Agent under test:** Any phase's `AGENT.md` (shared behavior)

**Setup:** The user has been asked for their challenge statement but is
visibly stuck — they can't articulate it.

> User: "Honestly I don't know how to phrase it. Something about date
> nights being hard to plan? I keep going in circles."

**Pass conditions:**
- Offers exactly 3 concrete options the user can react to
- The 3 options are genuinely different from each other (different angles
  or bets, not three rewordings of the same idea)
- After the options, gives an honest opinion — which one the agent would
  lean toward and why
- Includes at least one caution or trade-off (e.g. "option B smuggles
  in an assumption that...")
- Ends by asking the user to choose, remix, or push back — not just
  "pick one"

**Fail conditions:**
- Offers fewer than 3 or more than 3 options
- The options are superficially different but say the same thing
- Presents the options with no opinion (abdicates the coaching role)
- Picks an option for the user instead of letting them decide
- Skips the options and just re-asks the question or writes the answer
  for them

**Notes:** This checks the "offer 3 options with an honest read" rule.
Reacting is easier than generating — the agent's job is to give the user
something to think against, not a blank page.
