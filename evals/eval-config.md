# Eval Config

## What's being measured

Not code output — persona fidelity. Every `AGENT.md` in this repo is a system
prompt for **Rasha**, the coach persona. Evals check whether a given prompt
(or an edit to one) still produces the behavior the persona promises:

- **One question at a time** — never bundles multiple questions into one message
- **Rejects vague answers** — pushes back and sharpens instead of moving on
- **Offers three options with an honest opinion** when the user is stuck
- **Stays in its lane** — redirects questions that belong to a different phase
  instead of answering them
- **Warm but not soft** — friendly tone, but doesn't rubber-stamp weak thinking

`cases/shared/` covers the behaviors above, which apply to all 8 phase agents.
`cases/<phase>/` covers behaviors specific to that phase (e.g. Kick Off's
"stay out of user segmentation" boundary).

## How it's scored

Each case is pass/fail against its own **pass conditions** / **fail
conditions**. No partial credit — if a fail condition triggers, the case
fails, even if the rest of the response is good.

A scorecard for a run is just the list of cases with a pass/fail next to
each, plus notes on anything borderline.

## Methodology (manual for now)

There's no code pipeline here, so running an eval is manual:

1. Paste the phase's `AGENT.md` system prompt into an AI tool.
2. Play out the scenario described in the case file.
3. Save the raw transcript to `results/<date>-<phase>-<version>/run-log.md`.
4. Score it against each case's pass/fail conditions in
   `results/<date>-<phase>-<version>/scorecard.md`.

This can be automated later (script calls the API, an LLM judge grades
against the same pass/fail conditions) if the manual process becomes a
bottleneck — not needed to get value from it today.

## Threshold

Before shipping a change to any `AGENT.md` system prompt: every case in
`cases/shared/` plus every case in that phase's `cases/<phase>/` must pass.
A prompt edit that breaks a previously-passing case is a regression, not a
style tweak — treat it like one.
