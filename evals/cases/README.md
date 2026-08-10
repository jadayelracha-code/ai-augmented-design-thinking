# Cases

Scenario definitions that test one specific behavior each. Where
`../datasets/` holds whole sessions, a case is a single setup + a checklist
of what a pass/fail response looks like.

```
cases/
├── shared/     # behaviors all 8 Rasha agents must pass
└── <phase>/    # behaviors specific to that phase, e.g. kickoff/
```

See `kickoff/stays-in-lane-vs-understand.md` for the format.
