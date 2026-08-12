# Scorecard — Kick Off dry run v1

**Date:** 2026-08-12
**Agent:** `kickoff/AGENT.md` (system prompt, unmodified)
**Cases run:** 4 (1 kickoff-specific + 3 shared)

---

## Case 1: `kickoff/stays-in-lane-vs-understand` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Names it as good instinct / good thinking | Pass | ✅ | "great instinct," "really good sign" |
| 2 | States plainly that pains/segmentation belongs to Understand | Pass | ✅ | "that's Understand territory" |
| 3 | Redirects back to the current Kick Off question (the team) | Pass | ✅ | Ends with the team question |
| 4 | Engages with segmentation as if it were the answer | Fail | ✅ Not triggered | Does not discuss busy parents |
| 5 | Silently folds it into scope/team | Fail | ✅ Not triggered | Explicitly flags mismatch |
| 6 | Tells user to drop the thought entirely | Fail | ✅ Not triggered | Parks it for Understand |

---

## Case 2: `shared/one-question-at-a-time` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Reflects the answer back briefly | Pass | ✅ | Summarises gap + who's affected |
| 2 | Asks exactly ONE follow-up or next question | Pass | ✅ | One question about whose perspective |
| 3 | Does not dump a checklist/agenda | Pass | ✅ | No mention of upcoming topics |
| 4 | Bundles two+ questions into same message | Fail | ✅ Not triggered | Single question only |
| 5 | Lists full agenda unprompted | Fail | ✅ Not triggered | No agenda dump |
| 6 | Asks no question at all | Fail | ✅ Not triggered | Ends with a question |

---

## Case 3: `shared/rejects-vague-answer` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Acknowledges intent without dismissing | Pass | ✅ | "good place to start" |
| 2 | Names what's vague/broad | Pass | ✅ | "could mean a hundred different things" |
| 3 | Asks focused follow-up to sharpen | Pass | ✅ | Asks about specific touchpoint |
| 4 | Does NOT move on to next topic | Pass | ✅ | Stays on challenge statement |
| 5 | Accepts and moves on | Fail | ✅ Not triggered | Does not advance |
| 6 | Rewrites answer for the user | Fail | ✅ Not triggered | Asks, doesn't rewrite |
| 7 | Repeats same question verbatim | Fail | ✅ Not triggered | Fresh follow-up |
| 8 | Is harsh/dismissive | Fail | ✅ Not triggered | Kind tone throughout |

---

## Case 4: `shared/offers-three-options-with-opinion` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Offers exactly 3 options | Pass | ✅ | A, B, C |
| 2 | Options are genuinely different | Pass | ✅ | Logistics vs priorities vs relevance |
| 3 | Gives honest opinion with "why" | Pass | ✅ | Leans B, explains reasoning |
| 4 | Includes a caution/trade-off | Pass | ✅ | "could drift into better-marriage" |
| 5 | Asks user to choose/remix/push back | Pass | ✅ | "which feels closest" + "remix" |
| 6 | Fewer/more than 3 options | Fail | ✅ Not triggered | Exactly 3 |
| 7 | Options say the same thing | Fail | ✅ Not triggered | Genuinely different |
| 8 | No opinion given | Fail | ✅ Not triggered | Clear lean + reasoning |
| 9 | Picks for the user | Fail | ✅ Not triggered | User decides |
| 10 | Skips options entirely | Fail | ✅ Not triggered | Options provided |

---

## Case 5: `kickoff/progresses-through-all-sections` — FAIL

*Added after live interactive run with the user (not simulated).*

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Covers all six Kick Off sections | Pass | ❌ | Only reached Challenge + partial Scoping. Never got to Team, Stakeholders, Concept Map, Charette, or Readiness Check |
| 2 | Moves on once a section is genuinely answered | Pass | ❌ | Over-probed the challenge statement across 4+ turns even after user gave a usable answer |
| 3 | Tracks progress lightly | Pass | ❌ | No progress markers shown |
| 4 | Gets stuck on one section, never reaches later ones | Fail | ❌ TRIGGERED | Stuck on challenge sharpening for the entire conversation |
| 5 | Over-probes a section that's already answered | Fail | ❌ TRIGGERED | Kept asking "what's blocking them" after user had chosen a clear direction |

**Observations:**
- The agent correctly rejected vague answers and pushed back on
  solutions-as-challenge — those behaviors worked well.
- But the "never accept a vague answer" rule overpowered the "move on
  when it's genuinely answered" rule. The agent didn't recognise when
  "good enough for Kick Off" had been reached.
- The user had to flag this themselves — the agent showed no
  self-awareness that it was stuck.
- Borderline: the agent's challenge-sharpening questions got close to
  Understand territory (probing user blockers) but stayed just in-lane.

---

## Summary

| Case | Verdict |
|------|---------|
| `kickoff/stays-in-lane-vs-understand` | ✅ PASS (simulated) |
| `shared/one-question-at-a-time` | ✅ PASS (simulated) |
| `shared/rejects-vague-answer` | ✅ PASS (simulated) |
| `shared/offers-three-options-with-opinion` | ✅ PASS (simulated) |
| `kickoff/progresses-through-all-sections` | ❌ FAIL (live run) |

**Overall: 4/5 PASS, 1 FAIL — not clear to ship.**

The failing case is a coverage regression: the agent never completes the
full Kick Off sequence. The "don't accept vague answers" behavior works
but has no counterbalance telling the agent when an answer is solid
enough to move on. A prompt edit is needed before shipping.
