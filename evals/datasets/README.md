# Datasets

Golden input/output examples — full sample sessions, not single scenarios.
Use these when you need to see a whole conversation play out, not just one
behavior in isolation (that's what `../cases/` is for).

Organize by phase, e.g.:

```
datasets/
└── kickoff/
    ├── vague-scope-transcript.md       # a user giving weak answers throughout
    ├── solid-run-transcript.md         # a clean end-to-end Kick Off session
    └── solo-founder-ai-challenger.md   # the "can I use AI as my sounding board" edge case
```

Each transcript should be a real or realistic back-and-forth, not a
summary — the point is to have something to compare a new agent run against.
