# Scorecard — Kick Off dry run v2 (post-fix)

**Date:** 2026-08-12
**Agent:** `kickoff/AGENT.md` (with sharpening-cap and coverage-mandate fixes)
**Cases run:** 5 (2 kickoff-specific + 3 shared)

---

## Case 1: `kickoff/stays-in-lane-vs-understand` — PASS

Triggered naturally during the live run (user mentioned research planning
and workshop planning — agent parked both for Understand).

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Names it as good instinct / good thinking | Pass | ✅ | "Good instinct," "strong Understand-phase thinking" |
| 2 | States plainly that it belongs to Understand | Pass | ✅ | "That's Understand work, not Kick Off" |
| 3 | Redirects back to the current Kick Off question | Pass | ✅ | Returned to scoping / getting oriented each time |
| 4 | Engages with segmentation as the answer | Fail | ✅ Not triggered | Did not engage |
| 5 | Silently folds it in | Fail | ✅ Not triggered | Explicitly flagged |
| 6 | Tells user to drop the thought | Fail | ✅ Not triggered | Parked it |

---

## Case 2: `kickoff/progresses-through-all-sections` — PASS

Previously FAILED in v1. This was the fix target.

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Covers all six Kick Off sections | Pass | ✅ | Challenge → Scope → Team → Stakeholders → Getting Oriented → Readiness Check — all covered |
| 2 | Moves on once a section is genuinely answered | Pass | ✅ | Used 3-options for challenge instead of over-probing. Moved on after "looks good" for scope |
| 3 | Tracks progress lightly | Pass | ✅ | ✅ markers after each section |
| 4 | Gets stuck on one section | Fail | ✅ Not triggered | Progressed smoothly |
| 5 | Over-probes a section | Fail | ✅ Not triggered | Sharpening cap worked — offered options instead of drilling |

---

## Case 3: `shared/one-question-at-a-time` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Reflects the answer back briefly | Pass | ✅ | Consistently reflected before moving on |
| 2 | Asks exactly ONE follow-up or next question | Pass | ✅ | Single question per turn throughout |
| 3 | Does not dump a checklist/agenda | Pass | ✅ | No agenda dump until final summary |
| 4 | Bundles two+ questions | Fail | ✅ Not triggered | — |
| 5 | Lists full agenda unprompted | Fail | ✅ Not triggered | — |
| 6 | Asks no question at all | Fail | ✅ Not triggered | — |

---

## Case 4: `shared/rejects-vague-answer` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Acknowledges intent without dismissing | Pass | ✅ | "Meaningful space," "real edge" |
| 2 | Names what's vague/broad | Pass | ✅ | "A mission, not a design challenge yet" |
| 3 | Asks focused follow-up to sharpen | Pass | ✅ | Offered 3 options to react to |
| 4 | Does NOT move on to next topic | Pass | ✅ | Stayed on challenge until locked in |
| 5 | Accepts and moves on | Fail | ✅ Not triggered | — |
| 6 | Rewrites for the user | Fail | ✅ Not triggered | User chose from options |
| 7 | Repeats same question verbatim | Fail | ✅ Not triggered | — |
| 8 | Is harsh/dismissive | Fail | ✅ Not triggered | Warm throughout |

---

## Case 5: `shared/offers-three-options-with-opinion` — PASS

| # | Condition | Type | Result | Notes |
|---|-----------|------|--------|-------|
| 1 | Offers exactly 3 options | Pass | ✅ | A, B, C for challenge framing |
| 2 | Options are genuinely different | Pass | ✅ | First step vs translate expertise vs support system |
| 3 | Gives honest opinion with "why" | Pass | ✅ | Leaned A, explained reasoning |
| 4 | Includes a caution/trade-off | Pass | ✅ | "A could drift into 'build a course'" |
| 5 | Asks user to choose/remix/push back | Pass | ✅ | "Pick or grab a phrase from one" |
| 6 | Fewer/more than 3 | Fail | ✅ Not triggered | Exactly 3 |
| 7 | Options say the same thing | Fail | ✅ Not triggered | Genuinely different |
| 8 | No opinion given | Fail | ✅ Not triggered | Clear lean |
| 9 | Picks for the user | Fail | ✅ Not triggered | User decided |
| 10 | Skips options entirely | Fail | ✅ Not triggered | — |

---

## Summary

| Case | v1 | v2 |
|------|----|----|
| `kickoff/stays-in-lane-vs-understand` | ✅ PASS | ✅ PASS |
| `kickoff/progresses-through-all-sections` | ❌ FAIL | ✅ PASS |
| `shared/one-question-at-a-time` | ✅ PASS | ✅ PASS |
| `shared/rejects-vague-answer` | ✅ PASS | ✅ PASS |
| `shared/offers-three-options-with-opinion` | ✅ PASS | ✅ PASS |

**Overall: 5/5 PASS — kickoff agent is clear to ship.** 🎉

The prompt fix (sharpening cap + coverage mandate) resolved the v1
regression. The agent now progresses through all six sections without
getting stuck, while still pushing back on vague answers and staying in
its lane.
