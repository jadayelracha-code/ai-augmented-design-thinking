# Problem Space · Observe

> Goal: understand the *user*, not just the problem. Get out into the real world, talk to and watch actual people, and surface the jobs they're trying to get done, along with their pains and gains.

Understand told you what you *assume*. Observe is where you find out what's *true*. This is the phase where empathy is earned, through contact with real humans, not imagined ones.

> ⚠️ Still no solutions. You're here to learn about people, not pitch to them.

---

## Tools & methods in this phase

- **Doing research** — go where users are; combine talking, watching, and immersion.
- **In-depth interviews** — one-on-one conversations that surface stories and real past behavior.
- **Observations** — watch what people actually do, which often contradicts what they say.
- **Identify relevant jobs to be done, pains & gains** — the core JTBD lens:
  - **Jobs** — what is the user fundamentally trying to accomplish? (functional, emotional, social)
  - **Pains** — frustrations, obstacles, and risks in getting the job done today.
  - **Gains** — the outcomes and benefits they'd value, expected or delightful.
- **Empathy maps** — capture what a user says, thinks, does, and feels.
- **Storytelling** — turn raw observation into vivid, shareable narratives the team can act on.

---

## Where AI genuinely helps

**1. Synthesizing interviews at volume**
Turn many transcripts into candidate jobs, pains, and gains in minutes, which you then verify against the source quotes. Biggest time-saver of the whole phase.

**2. Building empathy maps from raw notes**
Feed AI a transcript and get a first-draft says/thinks/does/feels map to refine.

**3. Spotting patterns and contradictions**
Ask AI to surface recurring language, surprises, and places where what users *say* clashes with what they *do*.

**4. Drafting the story**
AI can shape your findings into a narrative, which you fact-check against the evidence.

---

## Where AI will mislead you

- It will confidently invent jobs, pains, and gains that sound plausible but aren't in your data. **Trace every one back to a specific quote or observation.**
- It flattens the messy, contradictory, emotional detail, which is often exactly where the real insight hides.
- It cannot sit in the room and feel the weight of what someone said. That's still on you.
- Empathy maps built purely from AI on thin data are fiction. The map is only as good as the real contact behind it.

---

## Ready-to-use prompts

**Prompt: Extract jobs, pains & gains from transcripts**
```
Below are [N] interview transcripts. Identify the user's:
- JOBS (what they're fundamentally trying to accomplish — functional, emotional, social)
- PAINS (frustrations, obstacles, risks today)
- GAINS (outcomes and benefits they'd value)
For each item, quote the specific line(s) that support it and note which
interview it came from. Do not include anything you can't tie to a direct quote.
Flag contradictions between what people say and what they appear to do.

[paste transcripts]
```

**Prompt: Draft an empathy map**
```
From this interview: [paste], draft an empathy map with four quadrants:
SAYS (direct quotes), THINKS (inferred, mark as inference), DOES (observed
actions), FEELS (emotional state, with the evidence). Keep inference clearly
separated from what was directly said or observed.
```

**Prompt: Turn findings into a story**
```
Here are my verified findings: [jobs/pains/gains with quotes]. Draft a short,
vivid narrative of one representative user's experience that the team can
rally around. Use only details grounded in the evidence — flag anything you'd
be adding for color so I can cut or verify it.
```

**Prompt: Challenge my interpretation**
```
Here's my read of what this user needs: [read]. Here's the raw quote: [quote].
Give me 2-3 alternative interpretations, and tell me what evidence would help
me tell them apart.
```

---

## Before moving to Point of View, check:

- [ ] Did I talk to and observe REAL people, not just imagine them?
- [ ] Can every job, pain, and gain be traced to a specific quote or observation?
- [ ] Did I capture what surprised me, not just what confirmed my hypotheses from Understand?
- [ ] Did I notice where what people SAY differs from what they DO?
- [ ] Do I have empathy grounded in evidence, or a tidy AI summary standing in for contact?

See [`TEMPLATE.md`](./TEMPLATE.md) for the observe worksheet, and [`AGENT.md`](./AGENT.md) for the portable Observe agent.
